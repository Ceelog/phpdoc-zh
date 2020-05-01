会话和安全
==========

**目录**

-   [会话管理基础](/session/security.html#会话管理基础)
-   [和会话安全相关的配置项](/session/security.html#和会话安全相关的配置项)

外部链接：<a href="http://www.acros.si/papers/session_fixation.pdf" class="link external">» 会话固定</a>

HTTP 会话管理是 web 应用安全的核心内容，
要采用尽可能的手段来确保会话安全。
开发人员应该合理的启用或使用可接受的设置。

会话管理基础
------------

### 会话安全

会话模块无法保证你存储在会话中的信息只能被创建会话的用户本人可见。
你需要采取额外的手段来保护会话中的机密信息，
至于采取何种方式来保护机密信息， 取决于你在会话中存储的数据的机密程度。

评估会话中存储的数据的重要性， 以及为此增加额外的保护机制，
通常需要付出一定的代价，同时会降低便利性。
例如，如果你需要保护用户免受社会工程学攻击， 你需要启用
*session.use\_only\_cookies* 选项。
这就要求用户在使用过程中，必须把浏览器设置为接受 cookie，
否则就无法正常使用会话功能了。

有很多种方式都可以导致会话 ID 被泄露给第三方。 例如，JavaScript
注入，URL 中包含会话 ID，数据包侦听， 或者直接访问你的物理设备等。
如果会话 ID 被泄漏给第三方， 那么他们就可以访问这个会话 ID
可以访问的全部资源。 首先，如果在 URL 中包含了会话 ID，
并且访问了外部的站点， 那么你的会话 ID
可能在外部站点的访问日志中被记录（referrer 请求头）。
另外，攻击者也可以监听你的网络通信，如果通信未加密， 那么会话 ID
将会在网络中以明文的形式进行传输。
针对这种情况的解决方案就是在服务端配置 SSL/TLS， 另外，使用 HSTS
可以达到更高的安全性。

> **Note**: <span class="simpara"> 即使使用 HTTPS
> 协议，也无法百分百保证机密数据不被泄漏。 例如，CRIME 和 BEAST
> 漏洞可以使得攻击者读取到你的数据。
> 另外，出于网络通信审计目的，很多网络中都存在 HTTPS MITM 代理，
> 可以读取 HTTPS 协议下的通信数据。
> 那么攻击者也可以搭建类似的代理服务器，用来窃取 HTTPS
> 协议下的通信数据。 </span>

### 严格会话管理

目前，默认情况下，PHP 是以自适应的方式来管理会话的，
这种方式使用起来很灵活，但是同样也带来了一定的风险。

从 PHP 5.5.2 开始，新增加了一个配置项：
<a href="/session/setup.html#" class="link">session.use_strict_mode</a>。
当启用这个配置项，并且你所用的会话存储处理器支持的话，未经初始化的会话
ID 会被拒绝，
并为其生成一个全新的会话，这可以避免攻击者使用一个已知的会话 ID
来进行攻击。 例如，攻击者可以通过邮件给受害者发送一个包含会话 ID
的链接： http://example.com/page.php?PHPSESSID=123456789。 如果启用了
<a href="/session/setup.html#" class="link">session.use_trans_sid</a>
配置项， 那么受害者将会使用攻击者所提供的会话 ID 开始一个新的会话。
如果启用了
<a href="/session/setup.html#" class="link">session.use_strict_mode</a>
选项，就可以降低风险。

**Warning**

用户自定义的会话存储器也可以通过实现会话 ID 验证来支持严格会话模式。
建议用户在实现自己的会话存储器的时候， 一定要对会话 ID
的合法性进行验证。

在浏览器一侧，可以为用来保存会话 ID 的 cookie 设置域，路径， 仅允许 HTTP
访问，必须使用 HTTPS 访问等安全属性。 如果使用的是 PHP 7.3.
版本，还可以对 cookie 设置 SameSite 属性。
攻击者可以利用浏览器的这些特性来设置永久可用的会话 ID。 仅仅设置
<a href="/session/setup.html#" class="link">session.use_only_cookies</a>
配置项 无法解决这个问题。而
<a href="/session/setup.html#" class="link">session.use_strict_mode</a>
配置项 可以降低这种风险。设置
<a href="/session/setup.html#" class="link">session.use_strict_mode</a>=On，
来拒绝未经初始化的会话 ID。

> **Note**: <span class="simpara"> 虽然使用
> <a href="/session/setup.html#" class="link">session.use_strict_mode</a>
> 配置项 可以降低灵活会话管理方式所带来的风险， 攻击者还是通过利用
> JavaScript 注入等手段，
> 强制用户使用由攻击者创建的并且经过了正常的初始化的会话 ID。
> 如何降低这种风向，可以参考本手册的建议部分。 </span> <span
> class="simpara"> 如果你已经启用了
> <a href="/session/setup.html#" class="link">session.use_strict_mode</a>
> 配置项， 同时使用基于时间戳的会话管理， 并且通过设置 <span
> class="function">session\_regenerate\_id</span> 配置项 来重新生成会话
> ID， 那么，攻击者生成的会话 ID 就可以被删除掉了。 </span> <span
> class="simpara"> 当发生对过期会话访问的时候，
> 你应该保存活跃会话的所有数据， 以备后续分析使用。
> 然后让用户退出当前的会话，并且重新登录。
> 防止攻击者继续使用“偷”来的会话。 </span>

**Warning**

对过期会话数据的访问并不总是意味着正在遭受攻击。
不稳定的网络状况，或者不正确的会话删除行为，
都会导致合法的用户产生访问过期会话数据的情况。

从 PHP 7.1.0 开始，增加了 <span
class="function">session\_create\_id</span> 函数。
这个函数允许开发者在会话 ID 中增加用户 ID 作为前缀，
以确保用户访问到正确对应的会话数据。 要使用这个函数， 请确保启用了
<a href="/session/setup.html#" class="link">session.use_strict_mode</a>
配置项， 否则恶意用户可能会伪造其他用户的会话 ID。

> **Note**: <span class="simpara"> 对于 PHP 7.1.0 之前的用户，应该使用
> CSPRNG（例如 /dev/urandom） 或者 <span
> class="function">random\_bytes</span> 函数以及哈希函数 来产生新的会话
> ID。 <span class="function">session\_create\_id</span>
> 函数本身包含碰撞检测的能力， 并且根据 INI
> 文件中和会话相关的配置项来生成会话 ID。 所以，建议使用 <span
> class="function">session\_create\_id</span> 函数来生成会话 ID。
> </span>

### 重新生成会话 ID

虽然
<a href="/session/setup.html#" class="link">session.use_strict_mode</a>
配置项可以降低风险，但是还不够。为了确保会话安全，开发者还需要使用 <span
class="function">session\_regenerate\_id</span> 函数。

会话 ID 重生机制可以有效的降低会话被窃取的风险， 所以，必须周期性的调用
<span class="function">session\_regenerate\_id</span> 函数
来重新生成会话 ID， 例如，对于机密内容，每隔 15 分钟就重新生成会话 ID。
这样一来，即使会话 ID 被窃取， 那么攻击者所得到的会话 ID
也会很快的过期， 如果他们进一步访问，就会产生对过期会话数据访问的错误。

当用户成功通过认证之后，*必须*为其重新生成会话 ID。 并且，必须在向
$\_SESSION 中保存用户认证信息之前 调用 <span
class="function">session\_regenerate\_id</span> 函数（ 从 PHP 7.0.0
开始， <span class="function">session\_regenerate\_id</span> 函数
会自动将重生之前的会话数据保存到新生成的会话）。
请确保只有新的会话包含用户认证信息。

开发者*不可*过分依赖
<a href="/session/setup.html#" class="link">session.gc_maxlifetime</a>
配置项。 因为攻击者可以在受害者的会话过期之前访问系统，
并且维持这个会话的活动，以保证这个会话不会过期。

实际上，你需要自己实现基于时间戳的会话数据管理机制。

**Warning**

虽然会话管理器可以透明的管理时间戳，但是这个特性尚未完整的实现。 在 GC
发生之前，旧的会话数据还得保存，
同时，开发者还得保证过期的会话数据已经被移除。
但是，开发者又不能立即移除活跃会话中的数据。
所以，不要同时在活跃会话上调用 *session\_regenerate\_id(true);* 和 <span
class="function">session\_destroy</span> 函数。
这听起来有点儿自相矛盾，但是事实上必须得这么做。

默认情况下，<span class="function">session\_regenerate\_id</span> 函数
*不会*删除旧的会话， 所以即使重生了会话 ID，旧的会话可能还是可用的。
开发者需要使用时间戳等机制， 来确保旧的会话数据不会再次被访问。

**Warning**

删除活跃会话可能会带来非预期的一些影响。
例如，在网络状态不稳定，或者有并发请求到达 Web 服务器的情况下，
立即删除活跃会话可能导致个别请求会话失效的问题。

立即删除活跃会话也无法检测可能存在的恶意访问。

作为替代方案， 你要在 $\_SESSION 中设置一个很短的过期时间，
然后根据这个时间戳来判断后续的访问是被允许的还是被禁止的。

在调用 <span class="function">session\_regenerate\_id</span> 函数之后，
不能立即禁止对旧的会话数据的访问，应该再一小段之间之后再禁止访问。
例如，在稳定的网络条件下，可以设置为几秒钟，
在不稳定的网络条件下，可以设置为几分钟。

如果用户访问了旧的会话数据（已经过期的）， 那么应该禁止访问。
建议从会话中移除这个用户的认证信息，因为这看起来像是在遭受攻击。

如果攻击者设置了不可删除的 cookie，那么使用
<a href="/session/setup.html#" class="link">session.use_only_cookies</a>
和 <span class="function">session\_regenerate\_id</span>
会导致正常用户遭受拒绝服务的问题。 如果发生这种情况，请让用户删除 cookie
并且警告用户他可能面临一些安全问题。 攻击者可以通过恶意的 Web
应用、浏览器插件以及对安全性较差的物理设备进行攻击 来伪造恶意的 cookie。

**Warning**

请勿误解这里的拒绝服务攻击风险所指的含义。 通常来讲，要保护会话 ID
的安全，*use\_strict\_mode=On* 是必须要做的。 建议所有的站点都启用
*use\_strict\_mode=On*。

只有当账号处于被攻击的时候，才会发生拒绝服务的问题。
通常都是由于应用中被注入了恶意的 JavaScript 才会导致这个问题。

### 会话中数据的删除

过期的会话中的数据应该是被删除的，并且不可访问。
现在的会话模块尚未很好的支持这种特性。

应该尽可能快的删除过期会话中的数据。 但是，活跃会话一定不要立即删除。
为了能够同时满足这两点要求，
你需要自己来实现基于时间戳的会话数据管理机制。

在 $\_SESSION 中设置会话过期时间戳，并且对其进行管理，
以便能够阻止对于过期会话的访问。
当发生对于过期会话的访问时，建议从相关用户的所有会话中删除认证信息，
并且要求用户重新认证。 对于过期会话数据的访问可能是一种攻击行为，
为了保护会话数据，你需要追踪每个用户的活跃会话。

> **Note**: <span class="simpara"> 当用户处于不稳定的网络，或者 web
> 应用存在并发的请求的时候， 也可能发生对于过期会话数据的访问。
> 服务器尝试为用户设置新的会话 ID， 但是很可能由于网络原因，导致
> Set-Cookie 的数据包无法到达用户的浏览器。 当通过 <span
> class="function">session\_regenerate\_id</span> 函数
> 为一个连接生成新的会话 ID 之后，其他的并发连接可能尚未得到这个新的会话
> ID。
> 因此，不能立即阻止对于过期会话数据的访问，而是要延迟一个很小的时间段，
> 这就是为什么我们需要实现基于时间戳的会话管理。 </span>

简而言之，不要在调用 <span
class="function">session\_regenerate\_id</span> 或者 <span
class="function">session\_destroy</span>
函数的时候立即删除旧的会话数据，
而是要通过一个时间戳来控制后续对于这个旧会话数据的访问。
从会话存储中删除数据的工作交给 <span class="function">session\_gc</span>
函数来完成吧。

### 会话和锁定

默认情况下，为了保证会话数据在多个请求之间的一致性，
对于会话数据的访问是加锁进行的。

但是，这种锁定机制也会导致被攻击者利用，来进行对于用户的拒绝服务攻击。
为了降低这种风险，请在访问会话数据的时候，尽可能的缩短锁定的时间。
当某个请求不需要更新会话数据的时候，使用只读模式访问会话数据。
也就是说，在调用 <span class="function">session\_start</span>
函数的时候， 使用 'read\_and\_close'
选项：*session\_start(\['read\_and\_close'=\>1\]);*。
另外，如果需要更新会话数据，那么在更新完毕之后， 马上调用 <span
class="function">session\_commit</span> 函数来释放对于会话数据的锁。

当会话不活跃的时候，当前的会话模块*不会检*测对于 $\_SESSION 的修改。
你需要自己来保证 在会话处于不活跃状态的时候，不要去修改它。

### 活跃会话

开发者需要自己来追踪每个用户的活跃会话，
要知道每个用户创建了多少活跃会话，每个活跃会话来自那个 IP 地址，
活跃了多长时间等。 PHP 不会自动完成这项工作，需要开发者来完成。

有很多种方式可以做到追踪用户的活跃会话。
你可以通过在数据库中存储会话信息来跟踪用户会话。
由于会话是可以被垃圾收集器收集掉的，
所以你也需要处理被收集掉的会话数据，
以保证数据库中的数据和真实的活跃会话数据的一致性。

一种很简单的方式就是使用“使用用户 ID 作为会话 ID
前缀”，并且保存必要的信息到 $\_SESSION 中。
大部分的数据库产品对于字符串前缀查询（译注：也即右模糊查询，可以利用索引）都有很好的性能表现。
为了实现这种方式，可以使用 <span
class="function">session\_regenerate\_id</span> 和 <span
class="function">session\_create\_id</span> 函数。

**Warning**

永远不要使用机密数据作为会话 ID 前缀！ 如果用户 ID
属于机密数据，那么可以考虑使用 <span class="function">hash\_hmac</span>
函数对其进行摘要后再使用。

**Warning**

必须启用
<a href="/session/setup.html#" class="link">session.use_strict_mode</a>
配置项。 请确保已经启用， 否则活跃会话数据库可能会被入侵。

要能够检测对于过期会话数据的访问，
基于时间戳的会话数据管理机制是必不可少的。
当检测到对于过期会话数据的访问时，你应该从相关用户的活跃会话中删除认证信息，
避免攻击者持续使用盗取的会话。

### 会话和自动登录

开发者不应该通过使用长生命周期的会话 ID 来实现自动登录功能，
因为这种方式提高了会话被窃取的风险。 开发者应该自己实现自动登录的机制。

在使用 <span class="function">setcookie</span>
的时候，传入安全的一次性摘要结果作为自动登录信息。 建议使用比 SHA-2
更高强度的摘要算法（例如 SHA-256） 对 <span
class="function">random\_bytes</span> 随机生成的数据 （也可以读取
/dev/urandom 设备）进行摘要作为自动登录的信息。

在用户访问的时候，如果发现用户尚未认证，
那么就去检查请求中是否包含了有效的一次性登录信息。
如果包含有效的一次性登录信息，那么就去认证用户，并且重新生成新的一次性登录信息。
自动登录的关键信息一定是只能使用一次，永远不要重复使用一次性登录信息。

自动登录信息是长生命周期的认证信息， 所以必须要尽可能的妥善保护。
可以对于自动登录信息对应的 cookie 设置路径、仅允许 HTTP
访问、仅允许安全访问 等属性来加以保护，并且仅在必需的时候才传送这个
cookie。

开发者也要提供禁用自动登录的机制，
以及删除不再需要的自动登录数据的能力。

### CSRF（跨站请求伪造）

会话和认证无法避免跨站请求伪造攻击。 开发者需要自己来实现保护应用不受
CSRF 攻击的功能。

<span class="function">output\_add\_rewrite\_var</span> 函数可以用来
保护应用免受 CSRF 攻击。更多信息请参考文档。

> **Note**: <span class="simpara"> PHP 7.2.0 之前的版本，这个函数和会话
> ID 使用了同样的输出缓冲以及 INI 设置项， 所以不建议在 PHP 7.2.0
> 之前使用 <span class="function">output\_add\_rewrite\_var</span>
> 函数。 </span>

大部分 Web 应用框架都提供了 CSRF 保护的特性。 详细信息请参考你所用的 Web
框架的文档。

从 PHP 7.3 开始，对于会话 cookie 增加了 SameSite 属性，
这个属性可以有效的降低 CSRF 攻击的风险。

和会话安全相关的配置项
----------------------

通过使用 INI 文件中和会话安全相关的配置项，来提高会话的安全性。
有一些重要的配置项没有默认值， 所以你需要自行设置。

-   <a href="/session/setup.html#" class="link">session.cookie_lifetime</a>=0

    *0* 表示特殊含义，它告知浏览器不要持久化存储 cookie 数据。
    也即，关闭浏览器的时候，会话 ID cookie 会被立即删除。
    如果将此项设置为非 0 的值， 可能会导致会话 ID 被其他用户使用。
    大部分应用应该把此项设置为 "*0*"。

    如果应用中有自动登录的功能， 请自行实现一种更加安全的方式，
    而不要使用长生命周期的会话 ID 来完成自动登录。
    至于如何实现安全的自动登录功能，请参考本文档前面的内容。

-   <a href="/session/setup.html#" class="link">session.use_cookies</a>=On

    <a href="/session/setup.html#" class="link">session.use_only_cookies</a>=On

    虽然 HTTP cookie 存在一些问题， 但是它确实是实现会话 ID
    管理的优选方案。 尽可能的仅使用 cookie 来进行会话 ID 管理，
    而且大部分应用也确实是只使用 cookie 来记录会话 ID 的。

    如果 *session.use\_only\_cookies*=Off， 会话模块会在基于 cookie
    的会话 ID 初始化之前 使用 GET/POST/URL 请求中的会话
    ID（如果存在的话）。

-   <a href="/session/setup.html#" class="link">session.use_strict_mode</a>=On

    虽然启用 *session.use\_strict\_mode*
    是必不可少的，但是默认情况下，这个配置项是未启用的。

    此设置防止会话模块使用未初始化的会话 ID。 也就是说，
    会话模块仅接受由它自己创建的有效的会话 ID，
    而拒绝由用户自己提供的会话 ID。

    攻击者可以自行设置 cookie 或者使用 JavaScript 注入的方式 来设置会话
    ID 进行攻击。 启用 *session.use\_strict\_mode* 配置项
    可以阻止使用未经会话模块初始化的会话 ID。

    > **Note**:
    >
    > 攻击者可以使用自己的设备产生会话 ID，也可以使用受害者的会话 ID。
    > 攻击者也可以通过一些后续操作保证会话活跃。 因此，启用
    > *session.use\_strict\_mode* 配置项 可以降低这种风险。

-   <a href="/session/setup.html#" class="link">session.cookie_httponly</a>=On

    禁止 JavaScript 访问会话 cookie。 此设置项可以保护 cookie 不被
    JavaScript 窃取。

    虽然可以使用会话 ID 来作为防范跨站请求伪造（CSRF）的关键数据，
    但是不建议你这么做。例如，攻击者可以把 HTML
    源代码保存下来并且发送给其他用户。 为了安全起见，开发者不应该在 web
    页面中显示会话 ID。 几乎所有的应用都应该对会话 ID cookie 设置
    httponly 为 On。

    > **Note**:
    >
    > 类似会话 ID，CSRF 保护串号也应该定期的更新。

-   <a href="/session/setup.html#" class="link">session.cookie_secure</a>=On

    仅允许在 HTTPS 协议下访问会话 ID cookie。 如果你的 web 站点仅支持
    HTTPS，那么必须将此配置项设置为 On。

    对于仅支持 HTTPS 的 web 站点建议考虑使用强制安全传输技术（HSTS）。

-   <a href="/session/setup.html#" class="link">session.cookie_samesite</a>="Lax"
    或者
    <a href="/session/setup.html#" class="link">session.cookie_samesite</a>="Strict"

    自 PHP 7.3 开始，可以为会话 cookie 设置 *"SameSite"* 属性。
    这个属性可以有效的降低 CSRF 攻击的风险。

    Lax 和 Strict 之间的区别是， 对于来自其他站点的并且携带了会话 cookie
    的 GET 请求的处理方式不同。 设置为 Lax
    会允许来自其他站点并且携带了会话 cookie 的请求， 设置为 Strict
    则不会允许这种请求访问本站的会话数据。

-   <a href="/session/setup.html#" class="link">session.gc_maxlifetime</a>=\[选择一个尽可能小的时间段\]

    *session.gc\_maxlifetime* 来设置删除过期会话数据的时间周期。
    *来*的删除，
    你需要自己来实现一套基于时间戳的会话数据生命周期管理机制。

    最好使用 <span class="function">session\_gc</span>
    函数来进行会话数据垃圾收集。 如果你是 UNIX 的操作系统， 最好使用类似
    cron 这样的定时任务来执行 <span class="function">session\_gc</span>
    函数。

    GC 的运行时机并不是精准的，带有一定的或然性，
    所以这个设置项并*不能*确保
    旧的会话数据被删除。某些会话存储处理模块不使用此设置项。
    更多的信息请参考会话存储模块的完整文档。
    虽然开发人员不能完全依赖这个设置，但是还是建议将其设置的尽可能的小。
    调整
    <a href="/session/setup.html#" class="link">session.gc_probability</a>
    和
    <a href="/session/setup.html#" class="link">session.gc_divisor</a>
    配置项 可以使得过期的会话数据在适当的周期内被删除。
    如果需要使用自动登录的功能， 请使用其他更加安全的方式自行实现，
    而不要通过使用长生命周期的会话 ID 来实现。

    > **Note**:
    >
    > 如果会话存储器将会话数据存储到 memcached 或者 mecache
    > 这种自带超时机制的存储中，
    > 就不依赖这个配置项来进行过期会话数据的垃圾收集。
    > 更多信息请参考对应的会话存储器文档。

-   <a href="/session/setup.html#" class="link">session.use_trans_sid</a>=Off

    如果你有需要，可以使用会话 ID 透传机制。 但是，禁用会话 ID
    透传机制可以 避免会话 ID 被注入以及泄漏， 有效的提高会话安全性。

    > **Note**:
    >
    > 会话 ID 可能在浏览器书签或者保存下来的 HTML 源代码中被泄漏。

-   <a href="/session/setup.html#" class="link">session.trans_sid_tags</a>=\[限制标签\]

    （PHP 7.1.0 及以上）一般情况下，默认值就可以，
    你无需重写不需要的标签。 之前版本的 PHP 请使用
    <a href="/session/setup.html#" class="link">url_rewriter.tags</a>
    配置项。

-   <a href="/session/setup.html#" class="link">session.trans_sid_hosts</a>=\[限制的主机名\]

    （PHP 7.1.0 及以上）这个配置项设定允许进行会话 ID 透传的主机白名单。
    请勿在其中加入你不信任的主机。 如果此配置项为空， 则仅允许
    *$\_SERVER\['HTTP\_HOST'\]* 的站点进行会话 ID 透传。

-   <a href="/session/setup.html#" class="link">session.referer_check</a>=\[原始
    URL\]

    当启用
    <a href="/session/setup.html#" class="link">session.use_trans_sid</a>
    配置项的时候， 这个设置可以降低会话 ID 注入的风险。 如果你的站点是
    http://example.com/， 那么就把此项设置为 http://example.com/。
    需要注意的是，如果使用了 HTTPS 协议，
    那么浏览器在发起请求的时候不会包含 referrer 请求头。
    建议启用此配置项，虽然它并不是可靠的安全措施。

-   <a href="/session/setup.html#" class="link">session.cache_limiter</a>=nocache

    确保对于已经认证的会话，其 HTTP 内容不会被浏览器缓存。
    应该仅针对公开内容允许缓存， 否则将会面临内容泄露的风险。 即使 HTTP
    内容不包含敏感数据， 也可以把它设置为“private”。
    注意，“private”可能会导致客户端缓存私有数据。 仅在 HTTP
    内容中不包含任何私有数据的时候，可以使用“public”。

-   <a href="/session/setup.html#" class="link">session.sid_length</a>="48"

    （PHP 7.1.0 及更高版本）更长的会话 ID 可以得到更高的安全强度。
    建议开发者将会话 ID 的长度设置为不低于 32 个字符。 当
    <a href="/session/setup.html#" class="link">session.sid_bits_per_character</a>="5"
    时， 会话 ID 至少需要 26 个字符。

-   <a href="/session/setup.html#" class="link">session.sid_bits_per_character</a>="6"

    （PHP 7.1.0 及更高版本） 即使会话 ID 的长度设定不变， 更高的会话 ID
    比特位设置也会产生安全性更高的会话 ID。

-   <a href="/session/setup.html#" class="link">session.hash_function</a>="sha256"

    （PHP 7.1.0 及更高版本）高强度的哈希算法可以生成更高安全性的会话
    ID。 虽然说，即使是采用 MD5
    哈希算法，要想生成完全一致的哈希结果都是不太现实的，
    但是还是建议开发者使用 SHA-2 或者更高强度的哈希算法。
    比如，可以考虑使用 sha384 和 sha512 哈希算法。 请确保
    <a href="/session/setup.html#" class="link">entropy</a>
    配置项的设置可以满足你所用的哈希算法对种子长度要求。
