Sodium
======

**目录**

-   [简介](/intro/sodium.html)
-   [安装／配置](/sodium/setup.html)
    -   [需求](/sodium/setup.html#需求)
    -   [安装](/sodium/setup.html#安装)
    -   [运行时配置](/sodium/setup.html#运行时配置)
    -   [资源类型](/sodium/setup.html#资源类型)
-   [预定义常量](/sodium/constants.html)
-   [Sodium 函数](/ref/sodium.html)
    -   [sodium\_add](/ref/sodium.html#sodium_add) — Add large numbers
    -   [sodium\_base642bin](/ref/sodium.html#sodium_base642bin) —
        Description
    -   [sodium\_bin2base64](/ref/sodium.html#sodium_bin2base64) —
        Description
    -   [sodium\_bin2hex](/ref/sodium.html#sodium_bin2hex) — Encode to
        hexadecimal
    -   [sodium\_compare](/ref/sodium.html#sodium_compare) — Compare
        large numbers
    -   [sodium\_crypto\_aead\_aes256gcm\_decrypt](/ref/sodium.html#sodium_crypto_aead_aes256gcm_decrypt)
        — Decrypt in combined mode with precalculation
    -   [sodium\_crypto\_aead\_aes256gcm\_encrypt](/ref/sodium.html#sodium_crypto_aead_aes256gcm_encrypt)
        — Encrypt in combined mode with precalculation
    -   [sodium\_crypto\_aead\_aes256gcm\_is\_available](/ref/sodium.html#sodium_crypto_aead_aes256gcm_is_available)
        — Check if hardware supports AES256-GCM
    -   [sodium\_crypto\_aead\_aes256gcm\_keygen](/ref/sodium.html#sodium_crypto_aead_aes256gcm_keygen)
        — Get random bytes for key
    -   [sodium\_crypto\_aead\_chacha20poly1305\_decrypt](/ref/sodium.html#sodium_crypto_aead_chacha20poly1305_decrypt)
        — Verify that the ciphertext includes a valid tag
    -   [sodium\_crypto\_aead\_chacha20poly1305\_encrypt](/ref/sodium.html#sodium_crypto_aead_chacha20poly1305_encrypt)
        — Encrypt a message
    -   [sodium\_crypto\_aead\_chacha20poly1305\_ietf\_decrypt](/ref/sodium.html#sodium_crypto_aead_chacha20poly1305_ietf_decrypt)
        — Verify that the ciphertext includes a valid tag
    -   [sodium\_crypto\_aead\_chacha20poly1305\_ietf\_encrypt](/ref/sodium.html#sodium_crypto_aead_chacha20poly1305_ietf_encrypt)
        — Encrypt a message
    -   [sodium\_crypto\_aead\_chacha20poly1305\_ietf\_keygen](/ref/sodium.html#sodium_crypto_aead_chacha20poly1305_ietf_keygen)
        — Get random bytes for key
    -   [sodium\_crypto\_aead\_chacha20poly1305\_keygen](/ref/sodium.html#sodium_crypto_aead_chacha20poly1305_keygen)
        — Get random bytes for key
    -   [sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_decrypt](/ref/sodium.html#sodium_crypto_aead_xchacha20poly1305_ietf_decrypt)
        — Description
    -   [sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_encrypt](/ref/sodium.html#sodium_crypto_aead_xchacha20poly1305_ietf_encrypt)
        — Description
    -   [sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_keygen](/ref/sodium.html#sodium_crypto_aead_xchacha20poly1305_ietf_keygen)
        — Description
    -   [sodium\_crypto\_auth\_keygen](/ref/sodium.html#sodium_crypto_auth_keygen)
        — Get random bytes for key
    -   [sodium\_crypto\_auth\_verify](/ref/sodium.html#sodium_crypto_auth_verify)
        — Verifies that the tag is valid for the message
    -   [sodium\_crypto\_auth](/ref/sodium.html#sodium_crypto_auth) —
        Compute a tag for the message
    -   [sodium\_crypto\_box\_keypair\_from\_secretkey\_and\_publickey](/ref/sodium.html#sodium_crypto_box_keypair_from_secretkey_and_publickey)
        — Description
    -   [sodium\_crypto\_box\_keypair](/ref/sodium.html#sodium_crypto_box_keypair)
        — Randomly generate a secret key and a corresponding public key
    -   [sodium\_crypto\_box\_open](/ref/sodium.html#sodium_crypto_box_open)
        — Verify and decrypt a ciphertext
    -   [sodium\_crypto\_box\_publickey\_from\_secretkey](/ref/sodium.html#sodium_crypto_box_publickey_from_secretkey)
        — Description
    -   [sodium\_crypto\_box\_publickey](/ref/sodium.html#sodium_crypto_box_publickey)
        — Description
    -   [sodium\_crypto\_box\_seal\_open](/ref/sodium.html#sodium_crypto_box_seal_open)
        — Decrypt the ciphertext
    -   [sodium\_crypto\_box\_seal](/ref/sodium.html#sodium_crypto_box_seal)
        — Encrypt a message
    -   [sodium\_crypto\_box\_secretkey](/ref/sodium.html#sodium_crypto_box_secretkey)
        — Description
    -   [sodium\_crypto\_box\_seed\_keypair](/ref/sodium.html#sodium_crypto_box_seed_keypair)
        — Deterministically derive the key pair from a single key
    -   [sodium\_crypto\_box](/ref/sodium.html#sodium_crypto_box) —
        Encrypt a message
    -   [sodium\_crypto\_generichash\_final](/ref/sodium.html#sodium_crypto_generichash_final)
        — Complete the hash
    -   [sodium\_crypto\_generichash\_init](/ref/sodium.html#sodium_crypto_generichash_init)
        — Initialize a hash
    -   [sodium\_crypto\_generichash\_keygen](/ref/sodium.html#sodium_crypto_generichash_keygen)
        — Get random bytes for key
    -   [sodium\_crypto\_generichash\_update](/ref/sodium.html#sodium_crypto_generichash_update)
        — Add message to a hash
    -   [sodium\_crypto\_generichash](/ref/sodium.html#sodium_crypto_generichash)
        — Get a hash of the message
    -   [sodium\_crypto\_kdf\_derive\_from\_key](/ref/sodium.html#sodium_crypto_kdf_derive_from_key)
        — Derive a subkey
    -   [sodium\_crypto\_kdf\_keygen](/ref/sodium.html#sodium_crypto_kdf_keygen)
        — Get random bytes for key
    -   [sodium\_crypto\_kx\_client\_session\_keys](/ref/sodium.html#sodium_crypto_kx_client_session_keys)
        — Description
    -   [sodium\_crypto\_kx\_keypair](/ref/sodium.html#sodium_crypto_kx_keypair)
        — Creates a new sodium keypair
    -   [sodium\_crypto\_kx\_publickey](/ref/sodium.html#sodium_crypto_kx_publickey)
        — Description
    -   [sodium\_crypto\_kx\_secretkey](/ref/sodium.html#sodium_crypto_kx_secretkey)
        — Description
    -   [sodium\_crypto\_kx\_seed\_keypair](/ref/sodium.html#sodium_crypto_kx_seed_keypair)
        — Description
    -   [sodium\_crypto\_kx\_server\_session\_keys](/ref/sodium.html#sodium_crypto_kx_server_session_keys)
        — Description
    -   [sodium\_crypto\_pwhash\_scryptsalsa208sha256\_str\_verify](/ref/sodium.html#sodium_crypto_pwhash_scryptsalsa208sha256_str_verify)
        — Verify that the password is a valid password verification
        string
    -   [sodium\_crypto\_pwhash\_scryptsalsa208sha256\_str](/ref/sodium.html#sodium_crypto_pwhash_scryptsalsa208sha256_str)
        — Get an ASCII encoded hash
    -   [sodium\_crypto\_pwhash\_scryptsalsa208sha256](/ref/sodium.html#sodium_crypto_pwhash_scryptsalsa208sha256)
        — Derives a key from a password
    -   [sodium\_crypto\_pwhash\_str\_needs\_rehash](/ref/sodium.html#sodium_crypto_pwhash_str_needs_rehash)
        — Description
    -   [sodium\_crypto\_pwhash\_str\_verify](/ref/sodium.html#sodium_crypto_pwhash_str_verify)
        — Verifies that a password matches a hash
    -   [sodium\_crypto\_pwhash\_str](/ref/sodium.html#sodium_crypto_pwhash_str)
        — Get an ASCII-encoded hash
    -   [sodium\_crypto\_pwhash](/ref/sodium.html#sodium_crypto_pwhash)
        — Derive a key from a password
    -   [sodium\_crypto\_scalarmult\_base](/ref/sodium.html#sodium_crypto_scalarmult_base)
        — 别名 sodium\_crypto\_box\_publickey\_from\_secretkey
    -   [sodium\_crypto\_scalarmult](/ref/sodium.html#sodium_crypto_scalarmult)
        — Compute a shared secret given a user's secret key and another
        user's public key
    -   [sodium\_crypto\_secretbox\_keygen](/ref/sodium.html#sodium_crypto_secretbox_keygen)
        — Get random bytes for key
    -   [sodium\_crypto\_secretbox\_open](/ref/sodium.html#sodium_crypto_secretbox_open)
        — Verify and decrypt a ciphertext
    -   [sodium\_crypto\_secretbox](/ref/sodium.html#sodium_crypto_secretbox)
        — Encrypt a message
    -   [sodium\_crypto\_secretstream\_xchacha20poly1305\_init\_pull](/ref/sodium.html#sodium_crypto_secretstream_xchacha20poly1305_init_pull)
        — Description
    -   [sodium\_crypto\_secretstream\_xchacha20poly1305\_init\_push](/ref/sodium.html#sodium_crypto_secretstream_xchacha20poly1305_init_push)
        — Description
    -   [sodium\_crypto\_secretstream\_xchacha20poly1305\_keygen](/ref/sodium.html#sodium_crypto_secretstream_xchacha20poly1305_keygen)
        — Description
    -   [sodium\_crypto\_secretstream\_xchacha20poly1305\_pull](/ref/sodium.html#sodium_crypto_secretstream_xchacha20poly1305_pull)
        — Description
    -   [sodium\_crypto\_secretstream\_xchacha20poly1305\_push](/ref/sodium.html#sodium_crypto_secretstream_xchacha20poly1305_push)
        — Description
    -   [sodium\_crypto\_secretstream\_xchacha20poly1305\_rekey](/ref/sodium.html#sodium_crypto_secretstream_xchacha20poly1305_rekey)
        — Description
    -   [sodium\_crypto\_shorthash\_keygen](/ref/sodium.html#sodium_crypto_shorthash_keygen)
        — Get random bytes for key
    -   [sodium\_crypto\_shorthash](/ref/sodium.html#sodium_crypto_shorthash)
        — Compute a fixed-size fingerprint for the message
    -   [sodium\_crypto\_sign\_detached](/ref/sodium.html#sodium_crypto_sign_detached)
        — Sign the message
    -   [sodium\_crypto\_sign\_ed25519\_pk\_to\_curve25519](/ref/sodium.html#sodium_crypto_sign_ed25519_pk_to_curve25519)
        — Convert an Ed25519 public key to a Curve25519 public key
    -   [sodium\_crypto\_sign\_ed25519\_sk\_to\_curve25519](/ref/sodium.html#sodium_crypto_sign_ed25519_sk_to_curve25519)
        — Convert an Ed25519 secret key to a Curve25519 secret key
    -   [sodium\_crypto\_sign\_keypair\_from\_secretkey\_and\_publickey](/ref/sodium.html#sodium_crypto_sign_keypair_from_secretkey_and_publickey)
        — Description
    -   [sodium\_crypto\_sign\_keypair](/ref/sodium.html#sodium_crypto_sign_keypair)
        — Randomly generate a secret key and a corresponding public key
    -   [sodium\_crypto\_sign\_open](/ref/sodium.html#sodium_crypto_sign_open)
        — Check that the signed message has a valid signature
    -   [sodium\_crypto\_sign\_publickey\_from\_secretkey](/ref/sodium.html#sodium_crypto_sign_publickey_from_secretkey)
        — Extract the public key from the secret key
    -   [sodium\_crypto\_sign\_publickey](/ref/sodium.html#sodium_crypto_sign_publickey)
        — Description
    -   [sodium\_crypto\_sign\_secretkey](/ref/sodium.html#sodium_crypto_sign_secretkey)
        — Description
    -   [sodium\_crypto\_sign\_seed\_keypair](/ref/sodium.html#sodium_crypto_sign_seed_keypair)
        — Deterministically derive the key pair from a single key
    -   [sodium\_crypto\_sign\_verify\_detached](/ref/sodium.html#sodium_crypto_sign_verify_detached)
        — Verify signature for the message
    -   [sodium\_crypto\_sign](/ref/sodium.html#sodium_crypto_sign) —
        Sign a message
    -   [sodium\_crypto\_stream\_keygen](/ref/sodium.html#sodium_crypto_stream_keygen)
        — Get random bytes for key
    -   [sodium\_crypto\_stream\_xor](/ref/sodium.html#sodium_crypto_stream_xor)
        — Encrypt a message
    -   [sodium\_crypto\_stream](/ref/sodium.html#sodium_crypto_stream)
        — Generate a deterministic sequence of bytes from a seed
    -   [sodium\_hex2bin](/ref/sodium.html#sodium_hex2bin) — Decodes a
        hexadecimally encoded binary string
    -   [sodium\_increment](/ref/sodium.html#sodium_increment) —
        Increment large number
    -   [sodium\_memcmp](/ref/sodium.html#sodium_memcmp) — Test for
        equality in constant-time
    -   [sodium\_memzero](/ref/sodium.html#sodium_memzero) — Overwrite
        buf with zeros
    -   [sodium\_pad](/ref/sodium.html#sodium_pad) — Add padding data
    -   [sodium\_unpad](/ref/sodium.html#sodium_unpad) — Remove padding
        data
