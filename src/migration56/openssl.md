OpenSSL changes in PHP 5.6.x
----------------------------

### Stream wrappers now verify peer certificates and host names by default when using SSL/TLS

All encrypted client streams now enable peer verification by default. By
default, this will use OpenSSL's default CA bundle to verify the peer
certificate. In most cases, no changes will need to be made to
communicate with servers with valid SSL certificates, as distributors
generally configure OpenSSL to use known good CA bundles.

The default CA bundle may be overridden on a global basis by setting
either the openssl.cafile or openssl.capath configuration setting, or on
a per request basis by using the
<a href="/context/ssl.html#context.ssl.cafile" class="link"><code class="parameter">cafile</code></a>
or
<a href="/context/ssl.html#context.ssl.capath" class="link"><code class="parameter">capath</code></a>
context options.

While not recommended in general, it is possible to disable peer
certificate verification for a request by setting the
<a href="/context/ssl.html#context.ssl.verify-peer" class="link"><code class="parameter">verify_peer</code></a>
context option to **`false`**, and to disable peer name validation by
setting the
<a href="/context/ssl.html#context.ssl.verify-peer-name" class="link"><code class="parameter">verify_peer_name</code></a>
context option to **`false`**.

### Certificate fingerprints

Support has been added for extracting and verifying certificate
fingerprints. <span class="function">openssl\_x509\_fingerprint</span>
has been added to extract a fingerprint from an X.509 certificate, and
two <a href="/context/ssl.html" class="link">SSL stream context</a>
options have been added: *capture\_peer\_cert* to capture the peer's
X.509 certificate, and *peer\_fingerprint* to assert that the peer's
certificate should match the given fingerprint.

### Default ciphers updated

The default ciphers used by PHP have been updated to a more secure list
based on the
<a href="https://wiki.mozilla.org/Security/Server_Side_TLS#Recommended_Ciphersuite" class="link external">» Mozilla cipher recommendations</a>,
with two additional exclusions: anonymous Diffie-Hellman ciphers, and
RC4.

This list can be accessed via the new
**`OPENSSL_DEFAULT_STREAM_CIPHERS`** constant, and can be overridden (as
in previous PHP versions) by setting the
<a href="/context/ssl.html#context.ssl.ciphers" class="link"><code class="parameter">ciphers</code></a>
context option.

### Compression disabled by default

SSL/TLS compression has been disabled by default to mitigate the CRIME
attack. PHP 5.4.13 added a
<a href="/context/ssl.html#context.ssl.disable-compression" class="link"><code class="parameter">disable_compression</code></a>
context option to allow compression to be disabled: this is now set to
**`true`** (that is, compression is disabled) by default.

### Allow servers to prefer their cipher order

The `honor_cipher_order` SSL context option has been added to allow
encrypted stream servers to mitigate BEAST vulnerabilities by preferring
the server's ciphers to the client's.

### Access the negotiated protocol and cipher

The protocol and cipher that were negotiated for an encrypted stream can
now be accessed via <span
class="function">stream\_get\_meta\_data</span> or <span
class="function">stream\_context\_get\_options</span> when the
`capture_session_meta` SSL context option is set to **`true`**.

``` php
<?php
$ctx = stream_context_create(['ssl' => [
    'capture_session_meta' => TRUE
]]);
 
$html = file_get_contents('https://google.com/', FALSE, $ctx);
$meta = stream_context_get_options($ctx)['ssl']['session_meta'];
var_dump($meta);
?>
```

以上例程会输出：

    array(4) {
      ["protocol"]=>
      string(5) "TLSv1"
      ["cipher_name"]=>
      string(20) "ECDHE-RSA-AES128-SHA"
      ["cipher_bits"]=>
      int(128)
      ["cipher_version"]=>
      string(11) "TLSv1/SSLv3"
    }

### New options for perfect forward secrecy in encrypted stream servers

Encrypted client streams already support perfect forward secrecy, as it
is generally controlled by the server. PHP encrypted server streams
using certificates capable of perfect forward secrecy do not need to
take any additional action to enable PFS; however a number of new SSL
context options have been added to allow more control over PFS and deal
with any compatibility issues that may arise.

`ecdh_curve`  
This option allows the selection of a specific curve for use with ECDH
ciphers. If not specified, *prime256v1* will be used.

`dh_param`  
A path to a file containing parametrs for Diffie-Hellman key exchange,
such as that created by the following command:

``` shell
openssl dhparam -out /path/to/my/certs/dh-2048.pem 2048
```

`single_dh_use`  
If set to **`true`**, a new key pair will be created when using
Diffie-Hellman parameters, thereby improving forward secrecy.

`single_ecdh_use`  
If set to **`true`**, a new key pair will always be generated when ECDH
cipher suites are negotiated. This improves forward secrecy.

### SSL/TLS version selection

It is now possible to select specific versions of SSL and TLS via the
`crypto_method` SSL context option or by specifying a specific transport
when creating a stream wrapper (for example, by calling <span
class="function">stream\_socket\_client</span> or <span
class="function">stream\_socket\_server</span>).

The `crypto_method` SSL context option accepts a bitmask enumerating the
protocols that are permitted, as does the `crypto_type` of <span
class="function">stream\_socket\_enable\_crypto</span>.

| Protocol(s)            | Client flag                               | Server flag                               | Transport    |
|------------------------|-------------------------------------------|-------------------------------------------|--------------|
| Any TLS or SSL version | **`STREAM_CRYPTO_METHOD_ANY_CLIENT`**     | **`STREAM_CRYPTO_METHOD_ANY_SERVER`**     | *ssl://*     |
| Any TLS version        | **`STREAM_CRYPTO_METHOD_TLS_CLIENT`**     | **`STREAM_CRYPTO_METHOD_TLS_SERVER`**     | *tls://*     |
| TLS 1.0                | **`STREAM_CRYPTO_METHOD_TLSv1_0_CLIENT`** | **`STREAM_CRYPTO_METHOD_TLSv1_0_SERVER`** | *tlsv1.0://* |
| TLS 1.1                | **`STREAM_CRYPTO_METHOD_TLSv1_1_CLIENT`** | **`STREAM_CRYPTO_METHOD_TLSv1_1_SERVER`** | *tlsv1.1://* |
| TLS 1.2                | **`STREAM_CRYPTO_METHOD_TLSv1_2_CLIENT`** | **`STREAM_CRYPTO_METHOD_TLSv1_2_SERVER`** | *tlsv1.2://* |
| SSL 3                  | **`STREAM_CRYPTO_METHOD_SSLv3_CLIENT`**   | **`STREAM_CRYPTO_METHOD_SSLv3_SERVER`**   | *sslv3://*   |

``` php
<?php

// Requiring TLS 1.0 or better when using file_get_contents():
$ctx = stream_context_create([
    'ssl' => [
        'crypto_method' => STREAM_CRYPTO_METHOD_TLS_CLIENT,
    ],
]);
$html = file_get_contents('https://google.com/', false, $ctx);

// Requiring TLS 1.1 or 1.2:
$ctx = stream_context_create([
    'ssl' => [
        'crypto_method' => STREAM_CRYPTO_METHOD_TLSv1_1_CLIENT |
                           STREAM_CRYPTO_METHOD_TLSv1_2_CLIENT,
    ],
]);
$html = file_get_contents('https://google.com/', false, $ctx);

// Connecting using the tlsv1.2:// stream socket transport.
$sock = stream_socket_client('tlsv1.2://google.com:443/');

?>
```

### <span class="function">openssl\_get\_cert\_locations</span> added

The <span class="function">openssl\_get\_cert\_locations</span> function
has been added: it returns the default locations PHP will search when
looking for CA bundles.

``` php
<?php
var_dump(openssl_get_cert_locations());
?>
```

以上例程会输出：

    array(8) {
      ["default_cert_file"]=>
      string(21) "/etc/pki/tls/cert.pem"
      ["default_cert_file_env"]=>
      string(13) "SSL_CERT_FILE"
      ["default_cert_dir"]=>
      string(18) "/etc/pki/tls/certs"
      ["default_cert_dir_env"]=>
      string(12) "SSL_CERT_DIR"
      ["default_private_dir"]=>
      string(20) "/etc/pki/tls/private"
      ["default_default_cert_area"]=>
      string(12) "/etc/pki/tls"
      ["ini_cafile"]=>
      string(0) ""
      ["ini_capath"]=>
      string(0) ""
    }

### SPKI support

Support has been added for generating, extracting and verifying signed
public key and challenges (SPKAC). <span
class="function">openssl\_spki\_new</span>, <span
class="function">openssl\_spki\_verify</span>, <span
class="function">openssl\_spki\_export\_challenge</span>, and <span
class="function">openssl\_spki\_export</span> have been added to create,
verify export PEM public key and associated challenge from SPKAC's
generated from a *KeyGen* HTML5 element.

`openssl_spki_new`  
Generates a new SPKAC using private key, challenge string and hashing
algorithm.

``` php
<?php
$pkey = openssl_pkey_new();
openssl_pkey_export($pkey, 'secret passphrase');

$spkac = openssl_spki_new($pkey, 'challenge string');
?>
```

以上例程会输出：

    SPKAC=MIIBXjCByDCBnzANBgkqhkiG9w0BAQEFAAOBjQAwgYkCgYEA3L0IfUijj7+A8CPC8EmhcdNoe5fUAog7OrBdhn7EkxFButUp40P7+LiYiygYG1TmoI/a5EgsLU3s9twEz3hmgY9mYIqb/rb+SF8qlD/K6KVyUORC7Wlz1Df4L8O3DuRGzx6/+3jIW6cPBpfgH1sVuYS1vDBsP/gMMIxwTsKJ4P0CAwEAARYkYjViMzYxMTktNjY5YS00ZDljLWEyYzctMGZjNGFhMjVlMmE2MA0GCSqGSIb3DQEBAwUAA4GBAF7hu0ifzmjonhAak2FhhBRsKFDzXdKIkrWxVNe8e0bZzMrWOxFM/rqBgeH3/gtOUDRS5Fnzyq425UsTYbjfiKzxGeCYCQJb1KJ2V5Ij/mIJHZr53WYEXHQTNMGR8RPm7IxwVXVSHIgAfXsXZ9IXNbFbcaLRiSTr9/N4U+MXUWL7

`openssl_spki_verify`  
Verifies provided SPKAC.

``` php
<?php
$pkey = openssl_pkey_new();
openssl_pkey_export($pkey, 'secret passphrase');

$spkac = openssl_spki_new($pkey, 'challenge string');
var_dump(openssl_spki_verify($spkac));
?>
```

`openssl_spki_export_challenge`  
Exports associated challenge from provided SPKAC.

``` php
<?php
$pkey = openssl_pkey_new();
openssl_pkey_export($pkey, 'secret passphrase');

$spkac = openssl_spki_new($pkey, 'challenge string');
$challenge = openssl_spki_export_challenge($spkac):
echo $challenge;
?>
```

以上例程会输出：

    challenge string

`openssl_spki_export`  
Exports the PEM formatted RSA public key from SPKAC.

``` php
<?php
$pkey = openssl_pkey_new();
openssl_pkey_export($pkey, 'secret passphrase');

$spkac = openssl_spki_new($pkey, 'challenge string');
echo openssl_spki_export($spkac);
?>
```

以上例程会输出：

    -----BEGIN PUBLIC KEY-----
    MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQDcvQh9SKOPv4DwI8LwSaFx02h7
    l9QCiDs6sF2GfsSTEUG61SnjQ/v4uJiLKBgbVOagj9rkSCwtTez23ATPeGaBj2Zg
    ipv+tv5IXyqUP8ropXJQ5ELtbXPUN/gvw7cO5EbPHr/7eMhbpw8Gl+AfWxW5hLW8
    MGw/+AwwjHBOwong/QIDAQAB
    -----END PUBLIC KEY-----
