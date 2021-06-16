---
layout:     post
title:      spring-boot全局配置文件说明
subtitle:   持续更新
date:       2018-12-17
author:     LSC
header-img: img/post-bg-ios9-web.jpg
catalog: true
tags:
    - java
    - Spring Boot
---

>spring-boot全局配置文件说明

# spring-boot全局配置文件说明

```java

# ----------------------------------------
＃核心特性
# ----------------------------------------
 
#BANNER
banner.charset = UTF-8 ＃横幅文件编码。
banner.location = classpath：banner.txt ＃横幅文件位置。
banner.image.location = classpath：banner.gif ＃横幅图像文件位置（也可以使用jpg / png）。
banner.image.width = #crs 中横幅图像的宽度（默认为76）
banner.image.height = #crs 中横幅图像的高度（默认基于图像高度）
banner.image.margin = ＃字符中的左手图像边距（默认为2）
banner.image.invert = ＃如果对于黑暗的终端主题应该反转图像（默认为false）
 
＃LOGGING
logging.config = ＃日志配置文件的位置。例如，用于Logback的`classpath：logback.xml`
logging.exception-conversion-word =％wEx ＃记录异常时使用的转换字。
logging.file = ＃日志文件名。例如`myapp.log`
logging.level。* = ＃日志级别严重性映射。例如`logging.level.org.springframework = DEBUG`
logging.path = ＃日志文件的位置。例如`/ var / log`
logging.pattern.console = ＃用于输出到控制台的Appender模式。仅支持默认的logback设置。
logging.pattern.file = ＃用于输出到文件的Appender模式。仅支持默认的logback设置。
logging.pattern.level = ＃日志级别的Appender模式（默认％5p）。仅支持默认的logback设置。
logging.register-shutdown-hook = false ＃在日志记录系统初始化时为其注册一个shutdown hook。
 
＃AOP
spring.aop.auto = true ＃添加@EnableAspectJAutoProxy。
spring.aop.proxy-target-class = false ＃是否要创建基于子类的（CGLIB）代理（true），而不是基于标准Java接口的代理（false）。
 
#IDENTITY（ContextIdApplicationContextInitializer）
spring.application.index = #Application index。
spring.application.name = ＃应用程序名称。
 
＃ADMIN （SpringApplicationAdminJmxAutoConfiguration）
spring.application.admin.enabled = false ＃启用应用程序的管理功能。
spring.application.admin.jmx-name = org.springframework.boot：type = Admin，name = SpringApplication #JMX 应用程序管理员MBean的名称。
 
#AUTO-CONFIGURATION
spring.autoconfigure.exclude = ＃要排除的自动配置类。
 
#SPEING CORE
spring.beaninfo.ignore = true ＃跳过BeanInfo类的搜索。
 
#SPRING CACHE（CacheProperties）
spring.cache.cache-names = #Cmama 分隔的要创建的缓存名称列表（如果底层缓存管理器支持）。
spring.cache.caffeine.spec = ＃用于创建缓存的规范。有关规格格式的更多详细信息，请查看CaffeineSpec。
spring.cache.couchbase.expiration = 0 ＃条目到期时间（以毫秒为单位）。默认情况下，条目永不过期。
spring.cache.ehcache.config = ＃用于初始化EhCache的配置文件的位置。
spring.cache.guava.spec = ＃用于创建缓存的规范。有关规范格式的更多详细信息，请查看CacheBuilderSpec。
spring.cache.infinispan.config = ＃用于初始化Infinispan的配置文件的位置。
spring.cache.jcache.config = ＃用于初始化缓存管理器的配置文件的位置。
spring.cache.jcache.provider = #CachingProvider实现的完全限定名称，用于检索符合JSR-107的缓存管理器。只有在类路径上有多个JSR-107实现时才需要。
spring.cache.type = #Cache 类型，默认情况下根据环境自动检测。
 
#SPRING CONFIG  - 仅使用环境属性（ConfigFileApplicationListener）
spring.config.location = #Config 文件位置。
spring.config.name = application ＃配置文件名。
 
#HAZELCAST（HazelcastProperties）
spring.hazelcast.config = ＃用于初始化Hazelcast的配置文件的位置。
 
#PROJECT INFORMATION（ProjectInfoProperties）
spring.info.build.location = classpath：META-INF / build-info.properties ＃生成的build-info.properties文件的位置。
spring.info.git.location =类路径：git.properties 生成的git.properties文件＃所在。
 
#JMX
spring.jmx.default-domain = ＃JMX域名。
spring.jmx.enabled = true ＃将管理bean公开给JMX域。
spring.jmx.server = mbeanServer ＃MBeanServer bean name。
 
#Email （MailProperties）
spring.mail.default-encoding = UTF-8 ＃默认MimeMessage编码。
spring.mail.host = #SMTP 服务器主机。例如`smtp.example.com`
spring.mail.jndi-name = ＃会话JNDI名称。设置时，优先于其他邮件设置。
spring.mail.password = #SMTP 服务器的登录密码。
spring.mail.port = #SMTP 服务器端口。
spring.mail.properties。* = ＃其他JavaMail会话属性。
spring.mail.protocol = smtp ＃SMTP服务器使用的协议。
spring.mail.test-connection = false ＃测试邮件服务器在启动时是否可用。
spring.mail.username = #STP 服务器的登录用户。
 
#APPLING SETTINGS（SpringApplication）
spring.main.banner-mode = console ＃用于在应用程序运行时显示横幅的模式。
spring.main.sources = 要包含在ApplicationContext中的 #Sources （类名，包名或XML资源位置）。
spring.main.web-environment = ＃在Web环境中运行应用程序（默认情况下自动检测）。
 
#FILE 编码（FileEncodingApplicationListener）
spring.mandatory-file-encoding = ＃应用程序必须使用的预期字符编码。
 
#INTERNATIONALIZATION（MessageSourceAutoConfiguration）
spring.messages.always-use-message-format = false ＃设置是否始终应用MessageFormat规则，甚至解析不带参数的消息。
spring.messages.basename = messages ＃逗号分隔的basenames列表，每个都遵循ResourceBundle约定。
spring.messages.cache-seconds = -1 ＃加载的资源包文件缓存到期，以秒为单位。设置为-1时，捆绑包将永久缓存。
spring.messages.encoding = UTF-8 ＃消息包编码。
spring.messages.fallback-to-system-locale = true ＃设置是否在找不到特定区域设置的文件时回退到系统区域设置。
 
#OUTPUT
spring.output.ansi.enabled = detect ＃配置ANSI输出。
 
#PID文件（ApplicationPidFileWriter）
spring.pid.fail-on-write-error = ＃如果使用ApplicationPidFileWriter但它无法写入PID文件，则失败。
spring.pid.file = ＃要写入的PID文件的位置（如果使用ApplicationPidFileWriter）。
 
#ProfILES
spring.profiles.active = ＃活动配置文件的逗号分隔列表（或列表，如果使用YAML）。
spring.profiles.include = ＃无条件激活指定的逗号分隔的配置文件（或使用YAML时的配置文件列表）。
 
#SENDGRID（SendGridAutoConfiguration）
spring.sendgrid.api-key = ＃SendGrid api key（用户名/密码的替代）
spring.sendgrid.username = ＃SendGrid帐户用户名
spring.sendgrid.password = ＃SendGrid帐户密码
spring.sendgrid.proxy.host = ＃SendGrid代理主机
spring.sendgrid.proxy.port = ＃SendGrid代理端口
 
 
# ----------------------------------------
#WEB PROPERTIES
# ----------------------------------------
 
#EmbEDDED SERVER CONFIGURATION（ServerProperties）
server.address = ＃服务器应绑定到的网络地址。
server.compression.enabled = false ＃如果启用了响应压缩。
server.compression.excluded-user-agents = ＃要从压缩中排除的用户代理列表。
server.compression.mime-types = ＃逗号分隔的应该压缩的MIME类型列表。例如`text / html，text / css，application / json`
server.compression.min-response-size = ＃执行压缩所需的最小响应大小。比如2048
server.connection-timeout = ＃连接器在关闭连接之前等待另一个HTTP请求的时间（以毫秒为单位）。未设置时，将使用连接器的特定于容器的默认值。使用值-1表示没有（即无限）超时。
server.context-parameters。* = ＃Servlet context init参数。例如`server.context-parameters.a = alpha`
server.context-path = ＃应用程序的上下文路径。
server.display-name = application ＃显示应用程序的名称。
server.max-http-header-size = 0 ＃HTTP消息头的最大字节数。
server.error.include-stacktrace = never ＃何时包含“stacktrace”属性。
server.error.path = / error ＃错误控制器的路径。
server.error.whitelabel.enabled = true ＃在服务器出错的情况下启用浏览器中显示的默认错误页面。
server.jetty.acceptors = ＃要使用的接受者线程数。
server.jetty.max-http-post-size = 0 #HTTP post或put内容的最大字节数。
server.jetty.selectors = ＃要使用的选择器线程数。
server.jsp-servlet.class-name = org.apache.jasper.servlet.JspServlet ＃JSP servlet的类名。
server.jsp-servlet.init-parameters。* = ＃用于配置JSP servlet的Init参数
server.jsp-servlet.registered = true ＃是否注册了JSP servlet
server.port = 8080 ＃服务器HTTP端口。
server.server-header = ＃用于服务器响应头的值（如果为空则不发送头）
server.servlet-path = / ＃主调度程序servlet的路径。
server.use-forward-headers = ＃如果X-Forwarded- *头应该应用于HttpRequest。
server.session.cookie.comment = ＃会话cookie的评论。
server.session.cookie.domain = ＃会话cookie的域名。
server.session.cookie.http-only = 会话cookie的＃“HttpOnly”标志。
server.session.cookie.max-age = ＃会话cookie的最大年龄，以秒为单位。
server.session.cookie.name = ＃会话cookie名称。
server.session.cookie.path = ＃会话cookie的路径。
server.session.cookie.secure = 会话cookie的＃“Secure”标志。
server.session.persistent = false ＃在重新启动之间保留会话数据。
server.session.store-dir = ＃用于存储会话数据的目录。
server.session.timeout = ＃会话超时，以秒为单位。
server.session.tracking-modes = ＃会话跟踪模式（以下一项或多项：“cookie”，“url”，“ssl”）。
server.ssl.ciphers = ＃支持的SSL密码。
server.ssl.client-auth = ＃是否需要客户端身份验证（“想要”）或需要（“需要”）。需要信任存储。
server.ssl.enabled = ＃启用SSL支持。
server.ssl.enabled-protocols = ＃启用SSL协议。
server.ssl.key-alias = ＃标识密钥库中密钥的别名。
server.ssl.key-password = ＃用于访问密钥库中密钥的密码。
server.ssl.key-store = ＃保存SSL证书的密钥库的路径（通常是jks文件）。
server.ssl.key-store-password = ＃用于访问密钥库的密码。
server.ssl.key-store-provider = ＃密钥库的提供者。
server.ssl.key-store-type = ＃密钥库的类型。
server.ssl.protocol = TLS ＃要使用的SSL协议。
server.ssl.trust-store = ＃持有SSL证书的信任存储。
server.ssl.trust-store-password = ＃用于访问信任库的密码。
server.ssl.trust-store-provider = ＃信任存储的提供者。
server.ssl.trust-store-type = ＃信任库的类型。
server.tomcat.accept-count = ＃当所有可能的请求处理线程都在使用时，传入连接请求的最大队列长度。
server.tomcat.accesslog.buffered = true ＃缓冲区输出，使其仅定期刷新。
server.tomcat.accesslog.directory = logs ＃创建日志文件的目录。可以相对于tomcat base dir还是绝对的。
server.tomcat.accesslog.enabled = false ＃启用访问日志。
server.tomcat.accesslog.pattern = common ＃访问日志的格式模式。
server.tomcat.accesslog.prefix = access_log ＃日志文件名前缀。
server.tomcat.accesslog.rename-on-rotate = false ＃推迟在文件名中包含日期戳，直到旋转时间。
server.tomcat.accesslog.request-attributes-enabled = false ＃设置用于请求的IP地址，主机名，协议和端口的请求属性。
server.tomcat.accesslog.rotate = true ＃启用访问日志轮换。
server.tomcat.accesslog.suffix = .log ＃日志文件名后缀。
server.tomcat.additional-tld-skip-patterns = ＃逗号分隔的其他模式列表，这些模式匹配要忽略的TLD扫描的jar。
server.tomcat.background-processor-delay = 30 ＃调用backgroundProcess方法之间的延迟（以秒为单位）。
server.tomcat.basedir = #Tomcat 基目录。如果未指定，将使用临时目录。
server.tomcat.internal-proxies = 10 \\。\\ d {1,3} \\。\\ d {1,3} \\。\\ d {1,3} | \\
        。192 \\ 168 \\ d {1,3} \\ d {1,3} | \\
        。169 \\ 254 \\ d {1,3} \\ d {1,3} | \\
        。127 \\ d {1,3} \\ d {1,3} \\ d {1,3} | \\
        172 \\ 1 [6-9] {1} \\ d {1,3} \\ d {1,3} |。。\\
        172 \\ 2 [0-9] {1} \\ d {1,3} \\ d {1,3} |。。\\
        172 \\。3 [0-1] {1} \\。\\ d {1,3} \\。\\ d {1,3} ＃正则表达式匹配可信IP地址。
server.tomcat.max-connections = ＃服务器在任何给定时间接受和处理的最大连接数。
server.tomcat.max-http-post-size = 0 #HTTP 帖子内容的最大字节数。
server.tomcat.max-threads = 0 ＃最大工作线程数。
server.tomcat.min-spare-threads = 0 ＃最小工作线程数。
server.tomcat.port-header = X-Forwarded-Port ＃用于覆盖原始端口值的HTTP标头的名称。
server.tomcat.protocol-header = ＃包含传入协议的标头，通常命名为“X-Forwarded-Proto”。
server.tomcat.protocol-header-https-value = https ＃协议标头的值，表示传入请求使用SSL。
server.tomcat.redirect-context-root = ＃是否应通过在路径中附加/来重定向对上下文根的请求。
server.tomcat.remote-ip-header = ＃从中提取远程ip的http头的名称。例如`X-FORWARDED-FOR`
server.tomcat.uri-encoding = UTF-8 ＃用于解码URI的字符编码。
server.undertow.accesslog.dir = #Undertow 访问日志目录。
server.undertow.accesslog.enabled = false ＃启用访问日志。
server.undertow.accesslog.pattern = common ＃访问日志的格式模式。
server.undertow.accesslog.prefix = access_log。＃日志文件名前缀。
server.undertow.accesslog.rotate = true ＃启用访问日志轮换。
server.undertow.accesslog.suffix = log ＃日志文件名后缀。
server.undertow.buffer-size = ＃每个缓冲区的大小（以字节为单位）。
server.undertow.buffers-per-region = ＃每个区域的缓冲区数。
server.undertow.direct-buffers = ＃在Java堆外部分配缓冲区。
server.undertow.io-threads = ＃为worker创建的I / O线程数。
server.undertow.max-http-post-size = 0 #HTTP 帖子内容的最大字节数。
server.undertow.worker-threads = ＃工作线程数。
 
#FREEMARKER（FreeMarkerAutoConfiguration）
spring.freemarker.allow-request-override = false ＃设置是否允许HttpServletRequest属性覆盖（隐藏）控制器生成的同名模型属性。
spring.freemarker.allow-session-override = false ＃设置是否允许HttpSession属性覆盖（隐藏）同名控制器生成的模型属性。
spring.freemarker.cache = false ＃启用模板缓存。
spring.freemarker.charset = UTF-8 ＃模板编码。
spring.freemarker.check-template-location = true ＃检查模板位置是否存在。
spring.freemarker.content-type = text / html ＃Content-Type value。
spring.freemarker.enabled = true ＃启用此技术的MVC视图分辨率。
spring.freemarker.expose-request-attributes = false ＃设置是否应在与模板合并之前将所有请求属性添加到模型中。
spring.freemarker.expose-session-attributes = false ＃设置是否应在与模板合并之前将所有HttpSession属性添加到模型中。
spring.freemarker.expose-spring-macro-helpers = true ＃设置是否公开一个RequestContext供Spring的宏库使用，名称为“springMacroRequestContext”。
spring.freemarker.prefer-file-system-access = true ＃首选文件系统访问模板加载。文件系统访问可以热检测模板更改。
spring.freemarker.prefix = ＃在构建URL时添加前缀以查看名称的前缀。
spring.freemarker.request-context-attribute = ＃所有视图的 RequestContext属性的名称。
spring.freemarker.settings。* = ＃众所周知的FreeMarker密钥将传递给FreeMarker的配置。
spring.freemarker.suffix = ＃在构建URL时附加到视图名称的后缀。
spring.freemarker.template-loader-path = classpath：/ templates / ＃逗号分隔的模板路径列表。
spring.freemarker.view-names = ＃可以解析的视图名称的白名单。
 
#CHROOVY TEMPLATES（GroovyTemplateAutoConfiguration）
spring.groovy.template.allow-request-override = false ＃设置是否允许HttpServletRequest属性覆盖（隐藏）控制器生成的同名模型属性。
spring.groovy.template.allow-session-override = false ＃设置是否允许HttpSession属性覆盖（隐藏）控制器生成的同名模型属性。
spring.groovy.template.cache = ＃启用模板缓存。
spring.groovy.template.charset = UTF-8 ＃模板编码。
spring.groovy.template.check-template-location = true ＃检查模板位置是否存在。
spring.groovy.template.configuration。* = ＃请参阅GroovyMarkupConfigurer
spring.groovy.template.content-type = test / html ＃Content-Type value。
spring.groovy.template.enabled = true ＃启用此技术的MVC视图分辨率。
spring.groovy.template.expose-request-attributes = false ＃设置是否应在与模板合并之前将所有请求属性添加到模型中。
spring.groovy.template.expose-session-attributes = false ＃设置是否应在与模板合并之前将所有HttpSession属性添加到模型中。
spring.groovy.template.expose-spring-macro-helpers = true ＃设置是否公开一个RequestContext供Spring的宏库使用，名称为“springMacroRequestContext”。
spring.groovy.template.prefix = ＃在构建URL时添加前缀以查看名称的前缀。
spring.groovy.template.request-context-attribute = ＃所有视图的 RequestContext属性的名称。
spring.groovy.template.resource-loader-path = classpath：/ templates / ＃Template path。
spring.groovy.template.suffix = .tpl ＃在构建URL时附加到视图名称的后缀。
spring.groovy.template.view-names = ＃可以解析的视图名称的白名单。
 
#SPRING HATEOAS（HateoasProperties）
spring.hateoas.use-hal-as-default-json-media-type = true ＃指定是否应将application / hal + json响应发送给接受application / json的请求。
 
#HTTP消息转换
spring.http.converters.preferred-json-mapper = jackson ＃用于HTTP消息转换的首选JSON映射器。设置为“gson”以强制使用Gson，当它和Jackson都在类路径上时。
 
#HTTP 编码（HttpEncodingProperties）
spring.http.encoding.charset = UTF-8 #HTTP 请求和响应的字符集。如果未明确设置，则添加到“Content-Type”标头。
spring.http.encoding.enabled = true ＃启用http编码支持。
spring.http.encoding.force = ＃强制编码到HTTP请求和响应上配置的字符集。
spring.http.encoding.force-request = ＃强制编码到HTTP请求的已配置字符集。未指定“force”时，默认为true。
spring.http.encoding.force-response = ＃强制编码到HTTP响应上配置的字符集。
spring.http.encoding.mapping = #Locale to Encoding mapping。
 
#MULTIPART（MultipartProperties）
spring.http.multipart.enabled = true ＃启用对多部分上传的支持。
spring.http.multipart.file-size-threshold = 0 ＃将文件写入磁盘的阈值。值可以使用后缀“MB”或“KB”来表示兆字节或千字节大小。
spring.http.multipart.location = ＃上传文件的中间位置。
spring.http.multipart.max-file-size = 1MB ＃最大文件大小。值可以使用后缀“MB”或“KB”来表示兆字节或千字节大小。
spring.http.multipart.max-request-size = 10MB ＃最大请求大小。值可以使用后缀“MB”或“KB”来表示兆字节或千字节大小。
spring.http.multipart.resolve-lazily = false ＃是否在文件或参数访问时懒惰地解决多部分请求。
 
#JACKSON （JacksonProperties）
spring.jackson.date-format = ＃日期格式字符串或完全限定的日期格式类名。例如`yyyy-MM-dd HH：mm：ss`。
spring.jackson.default-property-inclusion = ＃控制序列化期间包含的属性。
spring.jackson.deserialization。* = #Jackon on / off功能会影响Java对象的反序列化方式。
spring.jackson.generator。* = ＃Jackson开/关功能，适用于发电机。
spring.jackson.joda-date-time-format = #Joda日期时间格式字符串。如果未配置，如果使用格式字符串配置，则“date-format”将用作后备。
spring.jackson.locale = ＃用于格式化的区域设置。
spring.jackson.mapper。* = #Jackson 通用开/关功能。
spring.jackson.parser。* = ＃Jackson开启/关闭解析器的功能。
spring.jackson.property-naming-strategy = #Jackson PropertyNamingStrategy的常数之一。也可以是PropertyNamingStrategy子类的完全限定类名。
spring.jackson.serialization。* = #Jacker on / off功能会影响Java对象的序列化方式。
spring.jackson.time-zone = ＃格式化日期时使用的时区。例如`America / Los_Angeles`
 
#JERSEY （JerseyProperties）
spring.jersey.application-path = ＃作为应用程序基URI的路径。如果指定，则覆盖“@ApplicationPath”的值。
spring.jersey.filter.order = 0 ＃Jersey过滤链顺序。
spring.jersey.init。* = ＃通过servlet或过滤器传递给Jersey的Init参数。
spring.jersey.servlet.load-on-startup = -1 ＃加载Jersey servlet的启动优先级。
spring.jersey.type = servlet ＃Jersey集成类型。
 
#SPRING LDAP（LdapProperties）
spring.ldap.urls = ＃服务器的LDAP URL。
spring.ldap.base = #Base 后缀，所有操作都应该从中发起。
spring.ldap.username = ＃服务器的登录用户。
spring.ldap.password = ＃服务器的登录密码。
spring.ldap.base-environment。* = #LDAP 规范设置。
 
#EmbEDDED LDAP（EmbeddedLdapProperties）
spring.ldap.embedded.base-dn = ＃基本DN
spring.ldap.embedded.credential.username = ＃嵌入式LDAP用户名。
spring.ldap.embedded.credential.password = ＃嵌入式LDAP密码。
spring.ldap.embedded.ldif = classpath：schema.ldif #Schema （LDIF）脚本资源引用。
spring.ldap.embedded.port = ＃嵌入式LDAP端口。
spring.ldap.embedded.validation.enabled = true ＃启用LDAP模式验证。
spring.ldap.embedded.validation.schema = ＃自定义架构的路径。
 
#SPRING移动设备视图（DeviceDelegatingViewResolverAutoConfiguration）
spring.mobile.devicedelegatingviewresolver.enable-fallback = false ＃启用后备解析支持。
spring.mobile.devicedelegatingviewresolver.enabled = false ＃启用设备视图解析器。
spring.mobile.devicedelegatingviewresolver.mobile-prefix = mobile / ＃前缀用于查看移动设备名称的前缀。
spring.mobile.devicedelegatingviewresolver.mobile-suffix = ＃附加到移动设备的视图名称的后缀。
spring.mobile.devicedelegatingviewresolver.normal-prefix = ＃前缀用于查看普通设备的名称。
spring.mobile.devicedelegatingviewresolver.normal-suffix = ＃附加到普通设备的视图名称的后缀。
spring.mobile.devicedelegatingviewresolver.tablet-prefix = tablet / ＃前缀用于查看平板电脑设备名称的前缀。
spring.mobile.devicedelegatingviewresolver.tablet-suffix = ＃附加到平板电脑设备的视图名称的后缀。
 
#SPRING 移动网站首选项（SitePreferenceAutoConfiguration）
spring.mobile.sitepreference.enabled = true ＃启用SitePreferenceHandler。
 
#MUSTACHE TEMPLATES（MustacheAutoConfiguration）
spring.mustache.allow-request-override = ＃设置是否允许HttpServletRequest属性覆盖（隐藏）控制器生成的同名模型属性。
spring.mustache.allow-session-override = ＃设置是否允许HttpSession属性覆盖（隐藏）控制器生成的同名模型属性。
spring.mustache.cache = ＃启用模板缓存。
spring.mustache.charset = ＃模板编码。
spring.mustache.check-template-location = ＃检查模板位置是否存在。
spring.mustache.content-type = ＃Content-Type value。
spring.mustache.enabled = ＃启用此技术的MVC视图分辨率。
spring.mustache.expose-request-attributes = ＃设置是否应在与模板合并之前将所有请求属性添加到模型中。
spring.mustache.expose-session-attributes = ＃设置是否应在与模板合并之前将所有HttpSession属性添加到模型中。
spring.mustache.expose-spring-macro-helpers = ＃设置是否公开一个RequestContext供Spring的宏库使用，名称为“springMacroRequestContext”。
spring.mustache.prefix = classpath：/ templates / ＃适用于模板名称的前缀。
spring.mustache.request-context-attribute = ＃所有视图的 RequestContext属性的名称。
spring.mustache.suffix = .html #Shaffix 应用于模板名称。
spring.mustache.view-names = ＃可以解析的视图名称的白名单。
 
#SPRING MVC（WebMvcProperties）
spring.mvc.async.request-timeout = ＃异步请求处理超时之前的时间量（以毫秒为单位）。
spring.mvc.date-format = ＃要使用的日期格式。例如`dd / MM / yyyy`。
spring.mvc.dispatch-trace-request = false #Recatch对FrameworkServlet doService方法的TRACE请求。
spring.mvc.dispatch-options-request = true #Dispatch对FrameworkServlet doService方法的OPTIONS请求。
spring.mvc.favicon.enabled = true ＃启用favicon.ico的分辨率。
spring.mvc.formcontent.putfilter.enabled = true ＃启用Spring的HttpPutFormContentFilter。
spring.mvc.ignore-default-model-on-redirect = true ＃如果在重定向场景中应忽略“默认”模型的内容。
spring.mvc.locale = ＃要使用的语言环境。默认情况下，“Accept-Language”标头会覆盖此区域设置。
spring.mvc.locale-resolver = accept-header ＃定义应如何解析语言环境。
spring.mvc.log-resolved-exception = false ＃启用对“HandlerExceptionResolver”解析的异常的警告日志记录。
spring.mvc.media-types。* = ＃Maps用于内容协商的媒体类型的文件扩展名。
spring.mvc.message-codes-resolver-format = ＃格式化消息代码的策略。例如`PREFIX_ERROR_CODE`。
spring.mvc.servlet.load-on-startup = -1 ＃加载Spring Web Services servlet的启动优先级。
spring.mvc.static-path-pattern = / ** ＃用于静态资源的路径模式。
spring.mvc.throw-exception-if-no-handler-found = false ＃如果没有找到Handler来处理请求，则应该抛出“NoHandlerFoundException”。
spring.mvc.view.prefix = #Spring MVC视图前缀。
spring.mvc.view.suffix = #Spring MVC视图后缀。
 
#SPRING RESOURCES处理（ResourceProperties）
spring.resources.add-mappings = true ＃启用默认资源处理。
spring.resources.cache-period = ＃资源处理程序所服务资源的缓存周期，以秒为单位。
spring.resources.chain.cache = true ＃在资源链中启用缓存。
spring.resources.chain.enabled = ＃启用Spring资源处理链。默认情况下禁用，除非至少启用了一个策略。
spring.resources.chain.gzipped = false ＃启用已经gzip资源的解析。
spring.resources.chain.html-application-cache = false ＃启用HTML5应用程序缓存清单重写。
spring.resources.chain.strategy.content.enabled = false ＃启用内容版本策略。
spring.resources.chain.strategy.content.paths = / ** ＃逗号分隔的模式列表，应用于版本策略。
spring.resources.chain.strategy.fixed.enabled = false ＃启用固定版本策略。
spring.resources.chain.strategy.fixed.paths = / ** ＃以逗号分隔的模式列表应用于版本策略。
spring.resources.chain.strategy.fixed.version = ＃用于版本策略的版本字符串。
spring.resources.static-locations = classpath：/ META-INF / resources /，classpath：/ resources /，classpath：/ static /，classpath：/ public / ＃静态资源的位置。
 
#SPRING SESSION（SessionProperties）
spring.session.hazelcast.flush-mode = on-save ＃会话刷新模式。
spring.session.hazelcast.map-name = spring：session：sessions ＃用于存储会话的地图的名称。
spring.session.jdbc.initializer.enabled = ＃如有必要，在启动时创建所需的会话表。如果设置了默认表名称或配置了自定义架构，则会自动启用。
spring.session.jdbc.schema = classpath：org / springframework / session / jdbc / schema  -  @@ platform @@。sql ＃用于初始化数据库模式的SQL文件的路径。
spring.session.jdbc.table-name = SPRING_SESSION ＃用于存储会话的数据库表的名称。
spring.session.mongo.collection-name = sessions ＃用于存储会话的集合名称。
spring.session.redis.flush-mode = on-save #sessions flush mode。
spring.session.redis.namespace = ＃用于存储会话的密钥的命名空间。
spring.session.store-type = ＃会话商店类型。
 
#SPRING SOCIAL（SocialWebAutoConfiguration）
spring.social.auto-connection-views = false ＃启用支持的提供程序的连接状态视图。
 
#SPEING SOCIAL FACEBOOK（FacebookAutoConfiguration）
spring.social.facebook.app-id = ＃您的应用程序的Facebook App ID
spring.social.facebook.app-secret = ＃your application的Facebook App Secret
 
＃SPRING SOCIAL LINKEDIN（LinkedInAutoConfiguration）
spring.social.linkedin.app-id = ＃your application的LinkedIn App ID
spring.social.linkedin.app-secret = ＃your application的LinkedIn App Secret
 
#SPRING SOCIAL TWITTER（TwitterAutoConfiguration）
spring.social.twitter.app-id = ＃您的应用程序的Twitter应用程序ID
spring.social.twitter.app-secret = ＃your application的Twitter App Secret
 
#THYMELEAF（ThymeleafAutoConfiguration）
spring.thymeleaf.cache = true ＃启用模板缓存。
spring.thymeleaf.check-template = true ＃在呈现模板之前检查模板是否存在。
spring.thymeleaf.check-template-location = true ＃检查模板位置是否存在。
spring.thymeleaf.content-type = text / html ＃Content-Type value。
spring.thymeleaf.enabled = true ＃启用MVC Thymeleaf视图分辨率。
spring.thymeleaf.encoding = UTF-8 ＃模板编码。
spring.thymeleaf.excluded-view-names = ＃逗号分隔的视图名列表，应从分辨率中排除。
spring.thymeleaf.mode = HTML5 ＃要应用于模板的模板模式。另请参见StandardTemplateModeHandlers。
spring.thymeleaf.prefix = classpath：/ templates / ＃在构建URL时添加前缀以查看名称的前缀。
spring.thymeleaf.suffix = .html ＃在构建URL时附加到视图名称的后缀。
spring.thymeleaf.template-resolver-order = ＃链中模板解析器的顺序。
spring.thymeleaf.view-names = ＃逗号分隔的可以解析的视图名称列表。
 
#SPRING WEB服务（WebServicesProperties）
spring.webservices.path = / services ＃作为服务基URI的路径。
spring.webservices.servlet.init = ＃Servlet init参数传递给Spring Web Services。
spring.webservices.servlet.load-on-startup = -1 ＃加载Spring Web Services servlet的启动优先级。
 
 
 
# ----------------------------------------
＃安全属性
# ----------------------------------------
＃SECURITY（SecurityProperties）
security.basic.authorize-mode = role ＃要应用的安全授权模式。
security.basic.enabled = true ＃启用基本身份验证。
security.basic.path = / ** ＃逗号分隔的安全路径列表。
security.basic.realm = Spring ＃HTTP基本域名。
security.enable-csrf = false ＃启用跨站点请求伪造支持。
security.filter-order = 0 ＃安全过滤器链顺序。
security.filter-dispatcher-types = ASYNC，FORWARD，INCLUDE，REQUEST ＃安全过滤器链调度程序类型。
security.headers.cache = true ＃启用缓存控制HTTP标头。
security.headers.content-security-policy = ＃内容安全策略标头的值。
security.headers.content-security-policy-mode = default ＃内容安全策略模式。
security.headers.content-type = true ＃启用“X-Content-Type-Options”标头。
security.headers.frame = true ＃启用“X-Frame-Options”标头。
security.headers.hsts = all ＃HTTP严格传输安全（HSTS）模式（无，域，全部）。
security.headers.xss = true ＃启用跨站点脚本（XSS）保护。
security.ignored = ＃逗号分隔的要从默认安全路径中排除的路径列表。
security.require-ssl = false ＃为所有请求启用安全通道。
security.sessions =无状态＃会话创建策略（始终，从不，if_required，无状态）。
security.user.name = user ＃默认用户名。
security.user.password = ＃默认用户名的密码。默认情况下，启动时会记录随机密码。
security.user.role = USER ＃默认用户名的授予角色。
 
＃SECURITY OAUTH2客户端（OAuth2ClientProperties）
security.oauth2.client.client-id = ＃OAuth2客户端ID。
security.oauth2.client.client-secret = ＃OAuth2客户端密钥。默认情况下会生成随机密钥
 
＃SECURITY OAUTH2资源（ResourceServerProperties）
security.oauth2.resource.filter-order = ＃用于验证令牌的过滤器链的顺序。
security.oauth2.resource.id = ＃资源的标识符。
security.oauth2.resource.jwt.key-uri = #JWT令牌的URI。如果值不可用且密钥是公共的，则可以设置。
security.oauth2.resource.jwt.key-value = #JWT令牌的验证密钥。可以是对称密钥或PEM编码的RSA公钥。
security.oauth2.resource.prefer-token-info = true ＃使用令牌信息，可以设置为false以使用用户信息。
security.oauth2.resource.service-id = resource ＃
security.oauth2.resource.token-info-uri = 令牌解码端点的URI。
security.oauth2.resource.token-type = ＃使用userInfoUri时要发送的令牌类型。
security.oauth2.resource.user-info-uri = 用户端点的URI。
 
＃SECURITY OAUTH2 SSO（OAuth2SsoProperties）
security.oauth2.sso.filter-order = ＃如果不提供显式的WebSecurityConfigurerAdapter，则过滤要应用的顺序
security.oauth2.sso.login-path = / login ＃登录页面的路径，即触发重定向到OAuth2授权服务器的路径
 
 
# ----------------------------------------
#DATA PROPERTIES
# ----------------------------------------
 
#FLYWAY （FlywayProperties）
flyway.baseline-description = ＃
flyway.baseline-version = 1 ＃版本开始迁移
flyway.baseline-on-migrate = ＃
flyway.check-location = false ＃检查迁移脚本位置是否存在。
flyway.clean-on-validation-error = ＃
flyway.enabled = true ＃启用 flyway 。
flyway.encoding = ＃
flyway.ignore-failed-future-migration = ＃
flyway.init-sqls = ＃在获取连接后立即执行以初始化连接的SQL语句。
flyway.locations = classpath：db / migration ＃迁移脚本的位置
flyway.out-of-order = ＃
flyway.password = #JDBC 密码，如果你想让 Flyway 创建自己的DataSource
flyway.placeholder-prefix = ＃
flyway.placeholder-replacement = ＃
flyway.placeholder-suffix = ＃
flyway.placeholders。* = ＃
flyway.schemas = #schemas 要更新
flyway.sql-migration-prefix = V ＃
flyway.sql-migration-separator = ＃
flyway.sql-migration-suffix = .sql ＃
flyway.table = ＃
flyway.url = 要迁移的数据库的 #URN url。如果未设置，则使用主要配置的数据源。
flyway.user = ＃要迁移的数据库的登录用户。
flyway.validate-on-migrate = ＃
 
#LIQUIBASE（LiquibaseProperties）
liquibase.change-log = classpath：/db/changelog/db.changelog-master.yaml# 更改日志配置路径。
liquibase.check-change-log-location = true ＃检查更改日志位置是否存在。
liquibase.contexts = ＃逗号分隔的运行时上下文列表。
liquibase.default-schema = ＃默认数据库模式。
liquibase.drop-first = false ＃首先删除数据库模式。
liquibase.enabled = true ＃启用liquibase支持。
liquibase.labels = ＃逗号分隔的运行时标签列表。
liquibase.parameters。* = ＃更改日志参数。
liquibase.password = ＃要迁移的数据库的登录密码。
liquibase.rollback-file = ＃执行更新时将向其写入回滚SQL的文件。
liquibase.url = 要迁移的数据库的JDBC url。如果未设置，则使用主要配置的数据源。
liquibase.user = ＃要迁移的数据库的登录用户。
 
＃COUCHBASE（CouchbaseProperties）
spring.couchbase.bootstrap-hosts = #Cookbase 节点（主机或IP地址）来自引导程序。
spring.couchbase.bucket.name = default ＃要连接的存储桶的名称。
spring.couchbase.bucket.password =   ＃桶的密码。
spring.couchbase.env.endpoints.key-value = 1 ＃每个节点对Key / value服务的套接字数。
spring.couchbase.env.endpoints.query = 1 ＃针对Query（N1QL）服务的每个节点的套接字数。
spring.couchbase.env.endpoints.view = 1 ＃针对视图服务的每个节点的套接字数。
spring.couchbase.env.ssl.enabled = ＃启用SSL支持。除非另有说明，否则在提供“keyStore”时自动启用。
spring.couchbase.env.ssl.key-store = ＃保存证书的JVM密钥库的路径。
spring.couchbase.env.ssl.key-store-password = ＃用于访问密钥库的密码。
spring.couchbase.env.timeouts.connect = 5000 ＃桶连接超时（以毫秒为单位）。
spring.couchbase.env.timeouts.key-value = 2500 ＃阻止对特定密钥超时执行的操作（以毫秒为单位）。
spring.couchbase.env.timeouts.query = 7500 ＃N1QL查询操作超时（以毫秒为单位）。
spring.couchbase.env.timeouts.socket-connect = 1000 ＃套接字连接超时（以毫秒为单位）。
spring.couchbase.env.timeouts.view = 7500 ＃常规和地理空间视图操作超时（以毫秒为单位）。
 
# DAO (PersistenceExceptionTranslationAutoConfiguration)
spring.dao.exceptiontranslation.enabled = true ＃启用PersistenceExceptionTranslationPostProcessor。
 
#CASSANDRA（CassandraProperties）
spring.data.cassandra.cluster-name = #Cassandra 集群的名称。
spring.data.cassandra.compression = none ＃Cassandra二进制协议支持的压缩。
spring.data.cassandra.connect-timeout-millis = #Socket 选项：连接超时。
spring.data.cassandra.consistency-level = ＃查询一致性级别。
spring.data.cassandra.contact-points = localhost ＃逗号分隔的集群节点地址列表。
spring.data.cassandra.fetch-size = ＃查询默认提取大小。
spring.data.cassandra.keyspace-name = ＃要使用的Keyspace名称。
spring.data.cassandra.load-balancing-policy = ＃负载均衡策略的类名。
spring.data.cassandra.port = #Cassandra 服务器的端口。
spring.data.cassandra.password = ＃服务器的登录密码。
spring.data.cassandra.read-timeout-millis = #Socket 选项：读取超时。
spring.data.cassandra.reconnection-policy = ＃重新连接策略类。
spring.data.cassandra.retry-policy = ＃重试策略的类名。
spring.data.cassandra.serial-consistency-level = ＃查询串行一致性级别。
spring.data.cassandra.schema-action = none ＃启动时要采取的架构操作。
spring.data.cassandra.ssl = false ＃启用SSL支持。
spring.data.cassandra.username = ＃服务器的登录用户。
 
#DATA COUCHBASE（CouchbaseDataProperties）
spring.data.couchbase.auto-index = false ＃自动创建视图和索引。
spring.data.couchbase.consistency = read-your-own-writes ＃在生成的查询中默认应用的一致性。
spring.data.couchbase.repositories.enabled = true ＃启用Couchbase存储库。
 
#ELASTICSEARCH（ElasticsearchProperties）
spring.data.elasticsearch.cluster-name = elasticsearch ＃Elasticsearch集群名称。
spring.data.elasticsearch.cluster-nodes = ＃逗号分隔的集群节点地址列表。如果未指定，则启动客户机节点。
spring.data.elasticsearch.properties。* = ＃用于配置客户端的其他属性。
spring.data.elasticsearch.repositories.enabled = true ＃启用Elasticsearch存储库。
 
#DATA LDAP
spring.data.ldap.repositories.enabled = true ＃启用LDAP存储库。
 
#MONGODB（MongoProperties）
spring.data.mongodb.authentication-database = ＃认证数据库名称。
spring.data.mongodb.database = test ＃数据库名称。
spring.data.mongodb.field-naming-strategy = ＃要使用的FieldNamingStrategy的完全限定名称。
spring.data.mongodb.grid-fs-database = ＃GridFS数据库名称。
spring.data.mongodb.host = localhost #Mongo 服务器主机。不能用uri设置。
spring.data.mongodb.password = #mongo 服务器的登录密码。不能用uri设置。
spring.data.mongodb.port = 27017 #Mongo 服务器端口。不能用uri设置。
spring.data.mongodb.repositories.enabled = true ＃启用Mongo存储库。
spring.data.mongodb.uri = mongodb：// localhost / test ＃Mongo数据库URI。无法使用主机，端口和凭据进行设置。
spring.data.mongodb.username = #mongo 服务器的登录用户。不能用uri设置。
 
#DATA REDIS
spring.data.redis.repositories.enabled = true ＃启用Redis存储库。
 
＃NEO4J（Neo4jProperties）
spring.data.neo4j.compiler = ＃编译器使用。
spring.data.neo4j.embedded.enabled = true ＃如果嵌入式驱动程序可用，则启用嵌入模式。
spring.data.neo4j.open-in-view = false ＃注册OpenSessionInViewInterceptor。将Neo4j会话绑定到线程以进行整个请求处理。
spring.data.neo4j.password = ＃服务器的登录密码。
spring.data.neo4j.repositories.enabled = true ＃启用Neo4j存储库。
spring.data.neo4j.uri = 驱动程序使用的 #URL 。默认情况下自动检测。
spring.data.neo4j.username = ＃服务器的登录用户。
 
#DATA REST（RepositoryRestProperties）
spring.data.rest.base-path = #Spring Data REST用于公开存储库资源的基本路径。
spring.data.rest.default-page-size = ＃默认页面大小。
spring.data.rest.detection-strategy = default ＃用于确定暴露哪些存储库的策略。
spring.data.rest.enable-enum-translation = ＃通过Spring Data REST默认资源包启用枚举值转换。
spring.data.rest.limit-param-name = #URL 查询字符串参数的名称，该参数指示一次返回多少结果。
spring.data.rest.max-page-size = ＃最大页面大小。
spring.data.rest.page-param-name = #URL 查询字符串参数的名称，指示要返回的页面。
spring.data.rest.return-body-on-create = ＃在创建实体后返回响应正文。
spring.data.rest.return-body-on-update = ＃更新实体后返回响应正文。
spring.data.rest.sort-param-name = #URL 查询字符串参数的名称，指示对结果进行排序的方向。
 
#SOLR （SolrProperties）
spring.data.solr.host = http：//127.0.0.1：8983 / solr #Solr host。如果设置了“zk-host”，则忽略。
spring.data.solr.repositories.enabled = true ＃启用Solr存储库。
spring.data.solr.zk-host = ＃ZooKeeper主机地址，格式为HOST：PORT。
 
＃DATASOURCE（DataSourceAutoConfiguration＆ DataSourceProperties）
spring.datasource.continue-on-error = false ＃初始化数据库时，如果发生错误，请不要停止。
spring.datasource.data = #Data （DML）脚本资源引用。
spring.datasource.data-username = ＃执行DML脚本的数据库用户（如果不同）。
spring.datasource.data-password = ＃执行DML脚本的数据库的密码（如果不同）。
spring.datasource.dbcp2。* = #Commons DBCP2特定设置
spring.datasource.driver-class-name = #JDBC 驱动程序的完全限定名称。默认情况下，基于URL自动检测。
spring.datasource.generate-unique-name = false ＃生成随机数据源名称。
spring.datasource.hikari。* = ＃Hikari特定设置
spring.datasource.initialize = true ＃使用'data.sql'填充数据库。
spring.datasource.jmx-enabled = false ＃启用JMX支持（如果由基础池提供）。
spring.datasource.jndi-name = ＃JNDI数据源的位置。设置时将忽略类，URL，用户名和密码。
spring.datasource.name = testdb ＃数据源的名称。
spring.datasource.password = ＃数据库的登录密码。
spring.datasource.platform = all ＃在架构资源中使用的平台（架构 -  $ {platform} .sql）。
spring.datasource.schema = #Schema （DDL）脚本资源引用。
spring.datasource.schema-username = ＃执行DDL脚本的数据库用户（如果不同）。
spring.datasource.schema-password = ＃执行DDL脚本的数据库的密码（如果不同）。
spring.datasource.separator =; #SQL初始化脚本中的语句分隔符。
spring.datasource.sql-script-encoding = #SQL 脚本编码。
spring.datasource.tomcat。* = ＃Tomcat数据源特定设置
spring.datasource.type = ＃要使用的连接池实现的完全限定名称。默认情况下，它是从类路径中自动检测到的。
spring.datasource.url = ＃数据库的JDBC url。
spring.datasource.username =
 
#IS （Elasticsearch HTTP客户端）（IsProperties）
spring.elasticsearch.jest.connection-timeout = 3000 ＃连接超时（以毫秒为单位）。
spring.elasticsearch.jest.multi-threaded = true ＃启用来自多个执行线程的连接请求。
spring.elasticsearch.jest.password = ＃登录密码。
spring.elasticsearch.jest.proxy.host = #HTTP 客户端应使用的代理主机。
spring.elasticsearch.jest.proxy.port = #HTTP 客户端应使用的代理端口。
spring.elasticsearch.jest.read-timeout = 3000 ＃读取超时（以毫秒为单位）。
spring.elasticsearch.jest.uris = http：// localhost：9200 ＃要使用的Elasticsearch实例的逗号分隔列表。
spring.elasticsearch.jest.username = ＃登录用户。
 
＃H2 Web控制台（H2ConsoleProperties）
spring.h2.console.enabled = false ＃启用控制台。
spring.h2.console.path = / h2-console ＃控制台可用的路径。
spring.h2.console.settings.trace = false ＃启用跟踪输出。
spring.h2.console.settings.web-allow-others = false ＃启用远程访问。
 
#JOOQ （JooqAutoConfiguration）
spring.jooq.sql-dialect = ＃SQLDialect与配置的数据源通信时使用的JOOQ。例如`POSTGRES`
 
＃JPA （JpaBaseConfiguration， HibernateJpaAutoConfiguration）
spring.data.jpa.repositories.enabled = true ＃启用JPA存储库。
spring.jpa.database = ＃要操作的目标数据库，默认情况下自动检测。也可以使用“databasePlatform”属性进行设置。
spring.jpa.database-platform = ＃要操作的目标数据库的名称，默认情况下自动检测。也可以使用“Database”枚举来设置。
spring.jpa.generate-ddl = false ＃在启动时初始化架构。
spring.jpa.hibernate.ddl-auto = ＃DDL模式。这实际上是“hibernate.hbm2ddl.auto”属性的快捷方式。使用嵌入式数据库时默认为“create-drop”，否则为“none”。
spring.jpa.hibernate.naming.implicit-strategy = ＃Hibernate 5隐式命名策略完全限定名称。
spring.jpa.hibernate.naming.physical-strategy = ＃Hibernate 5物理命名策略完全限定名称。
spring.jpa.hibernate.naming.strategy = ＃Hibernate 4命名策略完全限定名称。Hibernate 5不支持。
spring.jpa.hibernate.use-new-id-generator-mappings = ＃使用Hibernate的较新的IdentifierGenerator进行AUTO，TABLE和SEQUENCE。
spring.jpa.open-in-view = true ＃注册OpenEntityManagerInViewInterceptor。将JPA EntityManager绑定到线程以进行整个请求处理。
spring.jpa.properties。* = ＃要在JPA提供程序上设置的其他本机属性。
spring.jpa.show -sql = false ＃启用SQL语句的日志记录。
 
＃JTA（JtaAutoConfiguration）
spring.jta.enabled = true ＃启用JTA支持。
spring.jta.log-dir = #Transaction logs目录。
spring.jta.transaction-manager-id = #Transaction manager唯一标识符。
 
#ATOMIKOS（AtomikosProperties）
spring.jta.atomikos.connectionfactory.borrow-connection-timeout = 30 ＃从池中借用连接的超时时间（秒）。
spring.jta.atomikos.connectionfactory.ignore-session-transacted-flag = true ＃在创建会话时是否忽略事务标志。
spring.jta.atomikos.connectionfactory.local-transaction-mode = false ＃是否需要本地事务。
spring.jta.atomikos.connectionfactory.maintenance-interval = 60 ＃池维护线程运行之间的时间（以秒为单位）。
spring.jta.atomikos.connectionfactory.max-idle-time = 60 ＃从池中清除连接的时间（以秒为单位）。
spring.jta.atomikos.connectionfactory.max-lifetime = 0 ＃连接在被销毁之前可以合并的时间（以秒为单位）。0表示没有限制。
spring.jta.atomikos.connectionfactory.max-pool-size = 1 ＃池的最大大小。
spring.jta.atomikos.connectionfactory.min-pool-size = 1 ＃池的最小大小。
spring.jta.atomikos.connectionfactory.reap-timeout = 0 ＃借用连接的reap超时（以秒为单位）。0表示没有限制。
spring.jta.atomikos.connectionfactory.unique-resource-name = jmsConnectionFactory ＃用于在恢复期间标识资源的唯一名称。
spring.jta.atomikos.datasource.borrow-connection-timeout = 30 ＃从池中借用连接的超时（以秒为单位）。
spring.jta.atomikos.datasource.default-isolation-level = ＃池提供的连接的默认隔离级别。
spring.jta.atomikos.datasource.login-timeout = ＃用于建立数据库连接的超时（以秒为单位）。
spring.jta.atomikos.datasource.maintenance-interval = 60 ＃池维护线程运行之间的时间（以秒为单位）。
spring.jta.atomikos.datasource.max-idle-time = 60 ＃从池中清除连接的时间（以秒为单位）。
spring.jta.atomikos.datasource.max-lifetime = 0 ＃连接在被销毁之前可以合并的时间（以秒为单位）。0表示没有限制。
spring.jta.atomikos.datasource.max-pool-size = 1 ＃池的最大大小。
spring.jta.atomikos.datasource.min-pool-size = 1 ＃池的最小大小。
spring.jta.atomikos.datasource.reap-timeout = 0 ＃借用连接的reap超时（以秒为单位）。0表示没有限制。
spring.jta.atomikos.datasource.test-query = ＃用于在返回连接之前验证连接的SQL查询或语句。
spring.jta.atomikos.datasource.unique-resource-name = dataSource ＃用于在恢复期间标识资源的唯一名称。
spring.jta.atomikos.properties.checkpoint-interval = 500 ＃检查点之间的间隔。
spring.jta.atomikos.properties.console-file-count = 1 ＃可以创建的调试日志文件数。
spring.jta.atomikos.properties.console-file-limit = -1 ＃调试日志文件中最多可以存储多少字节。
spring.jta.atomikos.properties.console-file-name = tm.out #Debug logs文件名。
spring.jta.atomikos.properties.console-log-level = warn #Console日志级别。
spring.jta.atomikos.properties.default-jta-timeout = 10000 #JTA事务的默认超时。
spring.jta.atomikos.properties.enable-logging = true ＃启用磁盘日志记录。
spring.jta.atomikos.properties.force-shutdown-on-vm-exit = false ＃指定VM关闭是否应触发事务核心的强制关闭。
spring.jta.atomikos.properties.log-base-dir = ＃应存储日志文件的目录。
spring.jta.atomikos.properties.log-base-name = tmlog ＃Transactions日志文件基名。
spring.jta.atomikos.properties.max-actives = 50 ＃最大活动事务数。
spring.jta.atomikos.properties.max-timeout = 300000 ＃事务允许的最大超时（以毫秒为单位）。
spring.jta.atomikos.properties.output-dir = ＃存储调试日志文件的目录。
spring.jta.atomikos.properties.serial-jta-transactions = true ＃指定是否应尽可能加入子事务。
spring.jta.atomikos.properties.service = ＃应该启动的事务管理器实现。
spring.jta.atomikos.properties.threaded-two-phase-commit = true ＃使用不同（和并发）线程对参与资源进行两阶段提交。
spring.jta.atomikos.properties.transaction-manager-unique-name = #Transaction manager的唯一名称。
 
＃BITRONIX
spring.jta.bitronix.connectionfactory.acquire-increment = 1 ＃增长池时要创建的连接数。
spring.jta.bitronix.connectionfactory.acquisition-interval = 1 ＃获取无效连接后再次尝试获取连接之前等待的时间（以秒为单位）。
spring.jta.bitronix.connectionfactory.acquisition-timeout = 30 ＃从池中获取连接的超时时间（秒）。
spring.jta.bitronix.connectionfactory.allow-local-transactions = true ＃事务管理器是否应该允许混合XA和非XA事务。
spring.jta.bitronix.connectionfactory.apply-transaction-timeout = false ＃是否应在XAResource登记时在XAResource上设置事务超时。
spring.jta.bitronix.connectionfactory.automatic-enlisting-enabled = true ＃是否应自动登记和退出资源。
spring.jta.bitronix.connectionfactory.cache-producer-consumers = true ＃是否应缓存生产者和消费者。
spring.jta.bitronix.connectionfactory.defer-connection-release = true ＃提供程序是否可以在同一连接上运行多个事务并支持事务交错。
spring.jta.bitronix.connectionfactory.ignore-recovery-failures = false ＃是否应忽略恢复失败。
spring.jta.bitronix.connectionfactory.max-idle-time = 60 ＃从池中清除连接的时间（以秒为单位）。
spring.jta.bitronix.connectionfactory.max-pool-size = 10 ＃池的最大大小。0表示没有限制。
spring.jta.bitronix.connectionfactory.min-pool-size = 0 ＃池的最小大小。
spring.jta.bitronix.connectionfactory.password = ＃用于连接到JMS提供程序的密码。
spring.jta.bitronix.connectionfactory.share-transaction-connections = false ＃是否可以在事务上下文中共享处于ACCESSIBLE状态的连接。
spring.jta.bitronix.connectionfactory.test-connections = true ＃从池中获取时是否应测试连接。
spring.jta.bitronix.connectionfactory.two-pc-ordering-position = 1 ＃此资源在两阶段提交期间应采取的位置（始终首先是Integer.MIN_VALUE，始终是最后一个是Integer.MAX_VALUE）。
spring.jta.bitronix.connectionfactory.unique-name = jmsConnectionFactory ＃用于在恢复期间标识资源的唯一名称。
spring.jta.bitronix.connectionfactory.use -tm -join = true在启动XAResources时是否应该使用TMJOIN。
spring.jta.bitronix.connectionfactory.user = ＃用于连接到JMS提供程序的用户。
spring.jta.bitronix.datasource.acquire-increment = 1 ＃在增长池时创建的连接数。
spring.jta.bitronix.datasource.acquisition-interval = 1 ＃获取无效连接后再次尝试获取连接之前等待的时间（以秒为单位）。
spring.jta.bitronix.datasource.acquisition-timeout = 30 ＃从池中获取连接的超时时间（秒）。
spring.jta.bitronix.datasource.allow-local-transactions = true ＃事务管理器是否应该允许混合XA和非XA事务。
spring.jta.bitronix.datasource.apply-transaction-timeout = false ＃是否应该在XAResource登记时在XAResource上设置事务超时。
spring.jta.bitronix.datasource.automatic-enlisting-enabled = true ＃是否应自动登记和退出资源。
spring.jta.bitronix.datasource.cursor-holdability = ＃连接的默认光标可保持性。
spring.jta.bitronix.datasource.defer-connection-release = true ＃数据库是否可以在同一连接上运行多个事务并支持事务交错。
spring.jta.bitronix.datasource.enable -jdbc4-connection-test = ＃从池中获取连接时是否调用Connection.isValid（）。
spring.jta.bitronix.datasource.ignore-recovery-failures = false ＃是否应忽略恢复失败。
spring.jta.bitronix.datasource.isolation-level = ＃连接的默认隔离级别。
spring.jta.bitronix.datasource.local-auto-commit = ＃本地事务的默认自动提交模式。
spring.jta.bitronix.datasource.login-timeout = ＃用于建立数据库连接的超时（以秒为单位）。
spring.jta.bitronix.datasource.max-idle-time = 60 ＃从池中清除连接的时间（以秒为单位）。
spring.jta.bitronix.datasource.max-pool-size = 10 ＃池的最大大小。0表示没有限制。
spring.jta.bitronix.datasource.min-pool-size = 0 ＃池的最小大小。
spring.jta.bitronix.datasource.prepared-statement-cache-size = 0 ＃预准备语句缓存的目标大小。0禁用缓存。
spring.jta.bitronix.datasource.share-transaction-connections = false ＃是否可以在事务上下文中共享处于ACCESSIBLE状态的连接。
spring.jta.bitronix.datasource.test-query = ＃用于在返回连接之前验证连接的SQL查询或语句。
spring.jta.bitronix.datasource.two-PC排序位置 = 1 ＃，这一资源应在两阶段提交（总是第一个是Integer.MIN_VALUE的，总是在最后上都是Integer.MAX_VALUE）采取这样的立场。
spring.jta.bitronix.datasource.unique-name = dataSource ＃用于在恢复期间标识资源的唯一名称。
spring.jta.bitronix.datasource.use -tm -join = true在启动XAResources时是否应该使用TMJOIN。
spring.jta.bitronix.properties.allow-multiple-lrc = false ＃允许多个LRC资源登记到同一个事务中。
spring.jta.bitronix.properties.asynchronous2-pc = false ＃启用两阶段提交的异步执行。
spring.jta.bitronix.properties.background-recovery-interval-seconds = 60 ＃在后台运行恢复过程的时间间隔（秒）。
spring.jta.bitronix.properties.current-node-only-recovery = true ＃仅恢复当前节点。
spring.jta.bitronix.properties.debug-zero-resource-transaction = false ＃记录在没有单个登记资源的情况下执行的事务的创建和提交调用堆栈。
spring.jta.bitronix.properties.default-transaction-timeout = 60 ＃默认事务超时（以秒为单位）。
spring.jta.bitronix.properties.disable -jmx = false ＃启用JMX支持。
spring.jta.bitronix.properties.exception-analyzer = ＃设置要使用的异常分析器实现的完全限定名称。
spring.jta.bitronix.properties.filter-log-status = false ＃启用日志过滤，以便只写入强制日志。
spring.jta.bitronix.properties.force-batching-enabled = true ＃设置磁盘强制是否已批处理。
spring.jta.bitronix.properties.forced-write-enabled = true ＃设置日志是否强制为磁盘。
spring.jta.bitronix.properties.graceful-shutdown-interval = 60 ＃TM在关闭时中止事务之前等待事务完成的最大秒数。
spring.jta.bitronix.properties.jndi-transaction-synchronization-registry-name = ＃TransactionSynchronizationRegistry的JNDI名称。
spring.jta.bitronix.properties.jndi-user-transaction-name = ＃UserTransaction的JNDI名称。
spring.jta.bitronix.properties.journal = disk ＃期刊的名称。可以是'disk'，'null'或类名。
spring.jta.bitronix.properties.log-part1-filename = btm1.tlog ＃日志的第一个片段的名称。
spring.jta.bitronix.properties.log-part2-filename = btm2.tlog ＃期刊的第二个片段的名称。
spring.jta.bitronix.properties.max-log-size-in-mb = 2 ＃日志片段的最大大小（兆字节）。
spring.jta.bitronix.properties.resource-configuration-filename = ＃ResourceLoader配置文件名。
spring.jta.bitronix.properties.server-id = ＃必须唯一标识此TM实例的ASCII ID。默认为机器的IP地址。
spring.jta.bitronix.properties.skip-corrupted-logs = false ＃跳过损坏的事务日志条目。
spring.jta.bitronix.properties.warn-about-zero-resource-transaction = true ＃为没有单个登记资源的事务记录警告。
 
#NARAYANA（NarayanaProperties）
spring.jta.narayana.default-timeout = 60 ＃以秒为单位的事务超时。
spring.jta.narayana.expiry-scanners = com.arjuna.ats.internal.arjuna.recovery.ExpiredTransactionStatusManagerScanner ＃逗号分隔的到期扫描程序列表。
spring.jta.narayana.log-dir = #Transaction 对象商店目录。
spring.jta.narayana.one-phase-commit = true ＃启用一阶段提交优化。
spring.jta.narayana.periodic-recovery-period = 120 ＃以秒为单位执行定期恢复扫描的时间间隔。
spring.jta.narayana.recovery-backoff-period = 10 ＃以秒为单位退回恢复扫描的第一和第二阶段之间的时间段。
spring.jta.narayana.recovery-db-pass = ＃恢复管理器使用的数据库密码。
spring.jta.narayana.recovery-db-user = ＃恢复管理器使用的数据库用户名。
spring.jta.narayana.recovery-jms-pass = ＃恢复管理器使用的JMS密码。
spring.jta.narayana.recovery-jms-user = ＃恢复管理器使用的JMS用户名。
spring.jta.narayana.recovery-modules = ＃逗号分隔的恢复模块列表。
spring.jta.narayana.transaction-manager-id = 1 ＃唯一的事务管理器标识。
spring.jta.narayana.xa-resource-orphan-filters = ＃逗号分隔的孤立过滤器列表。
 
#EmbEDDED MONGODB（EmbeddedMongoProperties）
spring.mongodb.embedded.features = SYNC_DELAY ＃逗号分隔的要启用的功能列表。
spring.mongodb.embedded.storage.database-dir = ＃用于数据存储的目录。
spring.mongodb.embedded.storage.oplog-size = #oplog的最大大小，以兆字节为单位。
spring.mongodb.embedded.storage.repl-set-name = ＃副本集的名称。
spring.mongodb.embedded.version = 2.6.10 ＃使用的Mongo版本。
 
#REDIS（RedisProperties）
spring.redis.cluster.max-redirects = ＃在群集中执行命令时要遵循的最大重定向数。
spring.redis.cluster.nodes = ＃逗号分隔的“host：port”对列表引导自。
spring.redis.database = 0 ＃连接工厂使用的数据库索引。
spring.redis.url = ＃连接URL，将覆盖主机，端口和密码（用户将被忽略），例如redis：// user：password@example.com：6379
spring.redis.host = localhost ＃Redis服务器主机。
spring.redis.password = ＃redis服务器的登录密码。
spring.redis.ssl = false ＃启用SSL支持。
spring.redis.pool.max-active = 8 ＃池在给定时间可以分配的最大连接数。使用负值无限制。
spring.redis.pool.max-idle = 8 ＃池中“空闲”连接的最大数量。使用负值表示无限数量的空闲连接。
spring.redis.pool.max-wait = -1 ＃在池耗尽时，在抛出异常之前，连接分配应阻塞的最长时间（以毫秒为单位）。使用负值无限期阻止。
spring.redis.pool.min-idle = 0 ＃目标是池中维护的最小空闲连接数。此设置仅在其为正时才有效。
spring.redis.port = 6379 ＃Redis服务器端口。
spring.redis.sentinel.master = #Redis服务器的名称。
spring.redis.sentinel.nodes = ＃逗号分隔的主机：端口对列表。
spring.redis.timeout = 0 ＃连接超时（以毫秒为单位）。
 
#TRANSACTION（TransactionProperties）
spring.transaction.default-timeout = ＃默认事务超时（以秒为单位）。
spring.transaction.rollback-on-commit-failure = ＃在提交失败时执行回滚。
 
 
 
# ----------------------------------------
＃集成属性
# ----------------------------------------
 
＃ACTIVEMQ（ActiveMQProperties）
spring.activemq.broker-url = ActiveMQ代理的URL。默认情况下自动生成。例如`tcp：// localhost：61616`
spring.activemq.in-memory = true ＃指定默认代理URL是否应在内存中。如果已指定显式代理，则忽略。
spring.activemq.password = ＃代理的登录密码。
spring.activemq.user = ＃代理的登录用户。
spring.activemq.packages.trust-all = false ＃信任所有包。
spring.activemq.packages.trusted = ＃逗号分隔的要信任的特定包列表（不信任所有包时）。
spring.activemq.pool.configuration。* = ＃请参阅PooledConnectionFactory。
spring.activemq.pool.enabled = false ＃是否应创建PooledConnectionFactory而不是常规ConnectionFactory。
spring.activemq.pool.expiry-timeout = 0 ＃连接到期超时（以毫秒为单位）。
spring.activemq.pool.idle-timeout = 30000 ＃连接空闲超时（以毫秒为单位）。
spring.activemq.pool.max-connections = 1 ＃池化连接的最大数量。
 
#ARTEMIS（Artemis Properties）
spring.artemis.embedded.cluster-password = ＃群集密码。默认情况下在启动时随机生成。
spring.artemis.embedded.data-directory = #Journal 文件目录。如果关闭持久性，则没有必要。
spring.artemis.embedded.enabled = true ＃如果Artemis服务器API可用，则启用嵌入模式。
spring.artemis.embedded.persistent = false ＃启用持久存储。
spring.artemis.embedded.queues = ＃逗号分隔的队列，在启动时创建。
spring.artemis.embedded.server-id = ＃服务器ID。默认情况下，使用自动递增的计数器。
spring.artemis.embedded.topics = ＃以逗号分隔的主题列表，在启动时创建。
spring.artemis.host = localhost ＃Artemis经纪人主持人。
spring.artemis.mode = ＃Artemis部署模式，默认自动检测。
spring.artemis.password = ＃代理的登录密码。
spring.artemis.port = 61616 #Artemis 经纪人端口。
spring.artemis.user = ＃代理的登录用户。
 
#SPRING BATCH（BatchProperties）
spring.batch.initializer.enabled = ＃如有必要，在启动时创建所需的批处理表。如果未设置自定义表前缀或配置了自定义架构，则自动启用。
spring.batch.job.enabled = true ＃在启动时执行上下文中的所有Spring Batch作业。
spring.batch.job.names = ＃逗号分隔的要在启动时执行的作业名称列表（例如`job1，job2`）。默认情况下，将执行上下文中找到的所有作业。
spring.batch.schema = classpath：org / springframework / batch / core / schema  -  @@ platform @@ .sql ＃用于初始化数据库模式的SQL文件的路径。
spring.batch.table-prefix = ＃所有批次元数据表的表前缀。
 
#JMS （JmsProperties）
spring.jms.jndi-name = ＃连接工厂JNDI名称。设置时，优先于其他连接工厂自动配置。
spring.jms.listener.acknowledge-mode = ＃容器的确认模式。默认情况下，侦听器使用自动确认进行事务处理。
spring.jms.listener.auto-startup = true ＃启动时自动启动容器。
spring.jms.listener.concurrency = ＃最小并发使用者数。
spring.jms.listener.max-concurrency = ＃最大并发使用者数。
spring.jms.pub-sub-domain = false ＃指定默认目标类型是否为topic。
spring.jms.template.default-destination = ＃在没有目标参数的发送/接收操作上使用的默认目标。
spring.jms.template.delivery-delay = ＃用于发送调用的传递延迟（以毫秒为单位）。
spring.jms.template.delivery-mode = ＃Delivery模式。设置时启用QoS。
spring.jms.template.priority = ＃发送时消息的优先级。设置时启用QoS。
spring.jms.template.qos-enabled = ＃发送消息时启用显式QoS。
spring.jms.template.receive-timeout = ＃用于接收呼叫的超时（以毫秒为单位）。
spring.jms.template.time-to-live = ＃以毫秒为单位发送消息的生存时间。设置时启用QoS。
 
#APACHE KAFKA（KafkaProperties）
spring.kafka.bootstrap-servers = ＃逗号分隔的主机：端口对列表，用于建立与Kafka集群的初始连接。
spring.kafka.client-id = #Id 在发出请求时传递给服务器; 用于服务器端日志记录。
spring.kafka.consumer.auto-commit-interval = ＃如果'enable.auto.commit'为true，则消费者偏移量自动提交给Kafka的频率（以毫秒为单位）。
spring.kafka.consumer.auto-offset-reset = ＃当Kafka中没有初始偏移量或服务器上当前偏移量不再存在时该怎么办。
spring.kafka.consumer.bootstrap-servers = ＃逗号分隔的主机：端口对列表，用于建立与Kafka集群的初始连接。
spring.kafka.consumer.client-id = #Id 在发出请求时传递给服务器; 用于服务器端日志记录。
spring.kafka.consumer.enable-auto-commit = ＃如果为true，则消费者的偏移量将在后台定期提交。
spring.kafka.consumer.fetch-max-wait = ＃如果没有足够的数据立即满足“fetch.min.bytes”给出的要求，服务器在回答获取请求之前将阻塞的最长时间（以毫秒为单位）。
spring.kafka.consumer.fetch-min-size = ＃服务器应以字节为单位返回获取请求的最小数据量。
spring.kafka.consumer.group-id = ＃唯一字符串，用于标识此使用者所属的使用者组。
spring.kafka.consumer.heartbeat-interval = ＃心跳与用户协调器之间的预期时间（以毫秒为单位）。
spring.kafka.consumer.key-deserializer = #Deserializer 类的键。
spring.kafka.consumer.max-poll-records = ＃一次调用poll（）时返回的最大记录数。
spring.kafka.consumer.value-deserializer = #Deserializer 类的值。
spring.kafka.listener.ack-count = ＃当ackMode为“COUNT”或“COUNT_TIME”时，偏移提交之间的记录数。
spring.kafka.listener.ack-mode = ＃Listener AckMode; 请参阅spring-kafka文档。
spring.kafka.listener.ack-time = ＃当ackMode为“TIME”或“COUNT_TIME”时，偏移提交之间的时间（以毫秒为单位）。
spring.kafka.listener.concurrency = ＃在侦听器容器中运行的线程数。
spring.kafka.listener.poll-timeout = ＃轮询使用者时使用的超时（以毫秒为单位）。
spring.kafka.producer.acks = ＃生产者要求领导者在考虑完成请求之前收到的确认数。
spring.kafka.producer.batch-size = ＃发送前批量记录的数量。
spring.kafka.producer.bootstrap-servers = ＃逗号分隔的主机：端口对列表，用于建立与Kafka集群的初始连接。
spring.kafka.producer.buffer-memory = ＃生产者可用于缓冲等待发送到服务器的记录的内存总字节数。
spring.kafka.producer.client-id = #Id 在发出请求时传递给服务器; 用于服务器端日志记录。
spring.kafka.producer.compression-type = ＃生产者生成的所有数据的压缩类型。
spring.kafka.producer.key-serializer = 键的序列化器类。
spring.kafka.producer.retries = ＃当大于零时，启用重试失败的发送。
spring.kafka.producer.value-serializer = #Serializer 类的值。
spring.kafka.properties。* = ＃用于配置客户端的其他属性。
spring.kafka.ssl.key-password = ＃密钥库文件中私钥的密码。
spring.kafka.ssl.keystore-location = ＃密钥库文件的位置。
spring.kafka.ssl.keystore-password = ＃存储密钥库文件的密码。
spring.kafka.ssl.truststore-location = ＃信任库文件的位置。
spring.kafka.ssl.truststore-password = ＃存储信任存储文件的密码。
spring.kafka.template.default-topic = ＃将消息发送到的默认主题。
 
#RABBIT（RabbitProperties）
spring.rabbitmq.addresses = ＃逗号分隔的客户端应连接的地址列表。
spring.rabbitmq.cache.channel.checkout-timeout = ＃达到缓存大小后等待获取通道的毫秒数。
spring.rabbitmq.cache.channel.size = ＃要在缓存中保留的通道数。
spring.rabbitmq.cache.connection.mode = channel ＃连接工厂缓存模式。
spring.rabbitmq.cache.connection.size = ＃缓存的连接数。
spring.rabbitmq.connection-timeout = ＃连接超时，以毫秒为单位; 零无限。
spring.rabbitmq.dynamic =真＃创建AmqpAdmin豆。
spring.rabbitmq.host = localhost ＃RabbitMQ主机。
spring.rabbitmq.listener.acknowledge-mode = ＃容器的确认模式。
spring.rabbitmq.listener.auto-startup = true ＃启动时自动启动容器。
spring.rabbitmq.listener.concurrency = ＃最小消费者数量。
spring.rabbitmq.listener.default-requeue-rejected = ＃是否重新排队交付失败; 默认`true`。
spring.rabbitmq.listener.idle-event-interval = ＃应该以毫秒为单位发布空闲容器事件的频率。
spring.rabbitmq.listener.max-concurrency = ＃最大消费者数量。
spring.rabbitmq.listener.prefetch = ＃单个请求中要处理的消息数。它应该大于或等于事务大小（如果使用）。
spring.rabbitmq.listener.retry.enabled = false ＃是否启用发布重试。
spring.rabbitmq.listener.retry.initial-interval = 1000 ＃传递消息的第一次和第二次尝试之间的间隔。
spring.rabbitmq.listener.retry.max-attempts = 3 ＃传递邮件的最大尝试次数。
spring.rabbitmq.listener.retry.max-interval = 10000 ＃尝试之间的最大间隔。
spring.rabbitmq.listener.retry.multiplier = 1.0 ＃应用于先前传递重试间隔的乘数。
spring.rabbitmq.listener.retry.stateless = true ＃重试是无状态还是有状态。
spring.rabbitmq.listener.transaction-size = ＃要在事务中处理的消息数。为获得最佳结果，它应小于或等于预取计数。
spring.rabbitmq.password = ＃登录以对代理进行身份验证。
spring.rabbitmq.port = 5672 ＃RabbitMQ端口。
spring.rabbitmq.publisher-confirms = false ＃启用发布者确认。
spring.rabbitmq.publisher-returns = false ＃启用发布者返回。
spring.rabbitmq.requested-heartbeat = ＃请求的心跳超时，以秒为单位; 零没有。
spring.rabbitmq.ssl.enabled = false ＃启用SSL支持。
spring.rabbitmq.ssl.key-store = ＃保存SSL证书的密钥库的路径。
spring.rabbitmq.ssl.key-store-password = ＃用于访问密钥库的密码。
spring.rabbitmq.ssl.trust-store = ＃持有SSL证书的信任存储。
spring.rabbitmq.ssl.trust-store-password = ＃用于访问信任库的密码。
spring.rabbitmq.ssl.algorithm = #SSL 算法使用。默认情况下，由Rabbit客户端库配置。
spring.rabbitmq.template.mandatory = false ＃启用强制消息。
spring.rabbitmq.template.receive-timeout = 0 ＃receive（）`方法的超时。
spring.rabbitmq.template.reply-timeout = 5000 #outoutout for sendAndReceive（）`方法。
spring.rabbitmq.template.retry.enabled = false ＃设置为true以在`RabbitTemplate`中启用重试。
spring.rabbitmq.template.retry.initial-interval = 1000 ＃第一次和第二次尝试发布消息之间的间隔。
spring.rabbitmq.template.retry.max-attempts = 3 ＃发布邮件的最大尝试次数。
spring.rabbitmq.template.retry.max-interval = 10000 ＃发布邮件的最大尝试次数。
spring.rabbitmq.template.retry.multiplier = 1.0 ＃应用于先前发布重试间隔的乘数。
spring.rabbitmq.username = ＃登录用户以对代理进行身份验证。
spring.rabbitmq.virtual-host = ＃连接到代理时使用的虚拟主机。
 
 
# ----------------------------------------
#TRTUATOR PROPERTIES
# ----------------------------------------
 
#ENDPOINTS（AbstractEndpoint子类）
endpoints.enabled = true ＃启用端点。
endpoints.sensitive = ＃默认端点敏感设置。
endpoints.actuator.enabled = true ＃启用端点。
endpoints.actuator.path = ＃端点URL路径。
endpoints.actuator.sensitive = false ＃在端点上启用安全性。
endpoints.auditevents.enabled = ＃启用端点。
endpoints.auditevents.path = ＃端点路径。
endpoints.auditevents.sensitive = false ＃在端点上启用安全性。
endpoints.autoconfig.enabled = ＃启用端点。
endpoints.autoconfig.id = ＃端点标识符。
endpoints.autoconfig.path = ＃端点路径。
endpoints.autoconfig.sensitive = ＃标记端点是否公开敏感信息。
endpoints.beans.enabled = ＃启用端点。
endpoints.beans.id = ＃端点标识符。
endpoints.beans.path = ＃端点路径。
endpoints.beans.sensitive = ＃标记端点是否公开敏感信息。
endpoints.configprops.enabled = ＃启用端点。
endpoints.configprops.id = ＃端点标识符。
endpoints.configprops.keys-to-sanitize = password，secret，key，token，。* credentials。*，vcap_services ＃应该清理的密钥。键可以是属性结尾的简单字符串或正则表达式。
endpoints.configprops.path = ＃端点路径。
endpoints.configprops.sensitive = ＃标记端点是否公开敏感信息。
endpoints.docs.curies.enabled = false ＃启用居里生成。
endpoints.docs.enabled = true ＃启用执行器docs端点。
endpoints.docs.path = / docs ＃
endpoints.docs.sensitive = false ＃
endpoints.dump.enabled = ＃启用端点。
endpoints.dump.id = ＃端点标识符。
endpoints.dump.path = ＃端点路径。
endpoints.dump.sensitive = ＃标记端点是否公开敏感信息。
endpoints.env.enabled = ＃启用端点。
endpoints.env.id = ＃端点标识符。
endpoints.env.keys-to-sanitize = password，secret，key，token，。* credentials。*，vcap_services ＃应该清理的密钥。键可以是属性结尾的简单字符串或正则表达式。
endpoints.env.path = ＃端点路径。
endpoints.env.sensitive = ＃标记端点是否公开敏感信息。
endpoints.flyway.enabled = ＃启用端点。
endpoints.flyway.id = ＃端点标识符。
endpoints.flyway.sensitive = ＃标记端点是否公开敏感信息。
endpoints.health.enabled = ＃启用端点。
endpoints.health.id = ＃端点标识符。
endpoints.health.mapping。* = ＃将健康状态映射到HttpStatus代码。默认情况下，已注册的运行状况映射到合理的默认值（即UP映射到200）。
endpoints.health.path = ＃端点路径。
endpoints.health.sensitive = ＃标记端点是否公开敏感信息。
endpoints.health.time-to-live = 1000 ＃缓存结果的生存时间（以毫秒为单位）。
endpoints.heapdump.enabled = ＃启用端点。
endpoints.heapdump.path = ＃端点路径。
endpoints.heapdump.sensitive = ＃标记端点是否公开敏感信息。
endpoints.hypermedia.enabled = false ＃为端点启用超媒体支持。
endpoints.info.enabled = ＃启用端点。
endpoints.info.id = ＃端点标识符。
endpoints.info.path = ＃端点路径。
endpoints.info.sensitive = ＃标记端点是否公开敏感信息。
endpoints.jolokia.enabled = true ＃启用Jolokia端点。
endpoints.jolokia.path = / jolokia ＃端点URL路径。
endpoints.jolokia.sensitive = true ＃在端点上启用安全性。
endpoints.liquibase.enabled = ＃启用端点。
endpoints.liquibase.id = ＃端点标识符。
endpoints.liquibase.sensitive = ＃标记端点是否公开敏感信息。
endpoints.logfile.enabled = true ＃启用端点。
endpoints.logfile.external-file = ＃要访问的外部日志文件。
endpoints.logfile.path = / logfile ＃端点URL路径。
endpoints.logfile.sensitive = true ＃在端点上启用安全性。
endpoints.loggers.enabled = true ＃启用端点。
endpoints.loggers.id = ＃端点标识符。
endpoints.loggers.path = / logfile ＃端点路径。
endpoints.loggers.sensitive = true ＃标记端点是否公开敏感信息。
endpoints.mappings.enabled = ＃启用端点。
endpoints.mappings.id = ＃端点标识符。
endpoints.mappings.path = ＃端点路径。
endpoints.mappings.sensitive = ＃标记端点是否公开敏感信息。
endpoints.metrics.enabled = ＃启用端点。
endpoints.metrics.filter.enabled = true ＃启用指标servlet过滤器。
endpoints.metrics.filter.gauge-submissions = merged ＃Http过滤规范提交（合并，每个http方法）
endpoints.metrics.filter.counter-submissions = merged ＃Http过滤器计数器提交（merged，per-http-method）
endpoints.metrics.id = ＃端点标识符。
endpoints.metrics.path = ＃端点路径。
endpoints.metrics.sensitive = ＃标记端点是否公开敏感信息。
endpoints.shutdown.enabled = ＃启用端点。
endpoints.shutdown.id = ＃端点标识符。
endpoints.shutdown.path = ＃端点路径。
endpoints.shutdown.sensitive = ＃标记端点是否公开敏感信息。
endpoints.trace.enabled = ＃启用端点。
endpoints.trace.id = ＃端点标识符。
endpoints.trace.path = ＃端点路径。
endpoints.trace.sensitive = ＃标记端点是否公开敏感信息。
 
#ENDPOINTS CORS CONFIGURATION（EndpointCorsProperties）
endpoints.cors.allow-credentials = ＃设置是否支持凭据。未设置时，不支持凭据。
endpoints.cors.allowed-headers = ＃逗号分隔的请求中允许的标头列表。'*'允许所有标题。
endpoints.cors.allowed-methods = GET ＃逗号分隔的允许方法列表。'*'允许所有方法。
endpoints.cors.allowed-origins = ＃逗号分隔的原始列表允许。'*'允许所有来源。未设置时，将禁用CORS支持。
endpoints.cors.exposed-headers = ＃逗号分隔的标题列表，包含在响应中。
endpoints.cors.max-age = 1800 ＃客户端可以缓存来自飞行前请求的响应的时间长度（以秒为单位）。
 
#JMX ENDPOINT（EndpointMBeanExportProperties）
endpoints.jmx.domain = ＃JMX域名。如果设置，则使用'spring.jmx.default-domain'的值初始化。
endpoints.jmx.enabled = true ＃启用所有端点的JMX导出。
endpoints.jmx.static-names = ＃附加的静态属性，附加到表示端点的MBean的所有ObjectName。
endpoints.jmx.unique-names = false ＃确保在发生冲突时修改ObjectNames。
 
#JOLOKIA（JolokiaProperties）
jolokia.config。* = ＃请参阅Jolokia手册
 
#MANAGEMENT HTTP SERVER（ManagementServerProperties）
management.add-application-context-header = true ＃在每个响应中添加“X-Application-Context”HTTP标头。
management.address = ＃管理端点应绑定到的网络地址。
management.context-path = ＃管理端点context-path。例如`/执行器'
management.cloudfoundry.enabled = ＃启用扩展的Cloud Foundry执行器端点
management.cloudfoundry.skip-ssl-validation = ＃跳过Cloud Foundry执行器端点安全调用的SSL验证
management.port = ＃管理端点HTTP端口。默认情况下，使用与应用程序相同的端口。配置其他端口以使用特定于管理的SSL。
management.security.enabled = true ＃启用安全性。
management.security.roles = ACTUATOR ＃可以访问管理端点的以逗号分隔的角色列表。
management.security.sessions =无状态＃会话创建要使用的策略（始终，从不，if_required，无状态）。
management.ssl.ciphers = ＃支持的SSL密码。需要自定义management.port。
management.ssl.client-auth = ＃是否需要客户端身份验证（“想要”）或需要（“需要”）。需要信任存储。需要自定义management.port。
management.ssl.enabled = ＃启用SSL支持。需要自定义management.port。
management.ssl.enabled-protocols = ＃启用SSL协议。需要自定义management.port。
management.ssl.key-alias = ＃标识密钥库中密钥的别名。需要自定义management.port。
management.ssl.key-password = ＃用于访问密钥库中密钥的密码。需要自定义management.port。
management.ssl.key-store = ＃保存SSL证书的密钥库的路径（通常是jks文件）。需要自定义management.port。
management.ssl.key-store-password = ＃用于访问密钥库的密码。需要自定义management.port。
management.ssl.key-store-provider = ＃密钥库的提供者。需要自定义management.port。
management.ssl.key-store-type = ＃密钥库的类型。需要自定义management.port。
management.ssl.protocol = TLS ＃要使用的SSL协议。需要自定义management.port。
management.ssl.trust-store = ＃持有SSL证书的信任存储。需要自定义management.port。
management.ssl.trust-store-password = ＃用于访问信任库的密码。需要自定义management.port。
management.ssl.trust-store-provider = ＃信任存储的提供者。需要自定义management.port。
management.ssl.trust-store-type = ＃信任库的类型。需要自定义management.port。
 
＃HEALTH指标
management.health.db.enabled = true ＃启用数据库运行状况检查。
management.health.cassandra.enabled = true ＃启用cassandra运行状况检查。
management.health.couchbase.enabled = true ＃启用couchbase运行状况检查。
management.health.defaults.enabled = true ＃启用默认健康指标。
management.health.diskspace.enabled = true ＃启用磁盘空间运行状况检查。
management.health.diskspace.path = ＃用于计算可用磁盘空间的路径。
management.health.diskspace.threshold = 0 ＃应该可用的最小磁盘空间（以字节为单位）。
management.health.elasticsearch.enabled = true ＃启用elasticsearch健康检查。
management.health.elasticsearch.indices = ＃逗号分隔的索引名称。
management.health.elasticsearch.response-timeout = 100 ＃等待群集响应的时间（以毫秒为单位）。
management.health.jms.enabled = true ＃启用JMS运行状况检查。
management.health.ldap.enabled = true ＃启用LDAP运行状况检查。
management.health.mail.enabled = true ＃启用邮件健康检查。
management.health.mongo.enabled = true ＃启用MongoDB运行状况检查。
management.health.rabbit.enabled = true ＃启用RabbitMQ运行状况检查。
management.health.redis.enabled = true ＃启用Redis运行状况检查。
management.health.solr.enabled = true ＃启用Solr运行状况检查。
management.health.status.order = DOWN，OUT_OF_SERVICE，UP，UNKNOWN ＃以逗号分隔的健康状态列表，按严重程度排序。
 
＃INFO CONTRIBUTORS（InfoContributorProperties）
management.info.build.enabled = true ＃启用构建信息。
management.info.defaults.enabled = true ＃启用默认信息贡献者。
management.info.env.enabled = true ＃启用环境信息。
management.info.git.enabled = true ＃启用git信息。
management.info.git.mode = simple ＃用于公开git信息的模式。
 
#REMOTE SHELL（ShellProperties）
management.shell.auth.type = simple ＃身份验证类型。根据环境自动检测。
management.shell.auth.jaas.domain = my-domain ＃JAAS domain。
management.shell.auth.key.path = ＃身份验证密钥的路径。这应该指向一个有效的“.pem”文件。
management.shell.auth.simple.user.name = user ＃登录用户。
management.shell.auth.simple.user.password = ＃登录密码。
management.shell.auth.spring.roles = ACTUATOR ＃以逗号分隔的登录CRaSH控制台所需角色的列表。
management.shell.command-path-patterns = classpath *：/ commands / **，classpath *：/ crash / commands / ** ＃用于查找命令的模式。
management.shell.command-refresh-interval = -1 ＃扫描更改并在必要时更新命令（以秒为单位）。
management.shell.config -path-patterns = classpath *：/ crash / * ＃用于查找配置的模式。
management.shell.disabled-commands = jpa *，jdbc *，jndi * ＃逗号分隔的要禁用的命令列表。
management.shell.disabled-plugins = ＃逗号分隔的要禁用的插件列表。默认情况下，某些插件会根据环境禁用。
management.shell.ssh.auth-timeout = ＃系统将提示用户再次登录后的毫秒数。
management.shell.ssh.enabled = true ＃启用CRaSH SSH支持。
management.shell.ssh.idle-timeout = ＃未使用的连接关闭之前的毫秒数。
management.shell.ssh.key-path = #SSH服务器密钥的路径。
management.shell.ssh.port = 2000 ＃SSH端口。
management.shell.telnet.enabled = false ＃启用CRaSH telnet支持。如果TelnetPlugin可用，则默认启用。
management.shell.telnet.port = 5000 ＃Telnet端口。
 
#TRACING（TraceProperties）
management.trace.include =请求标头，响应标头，cookie，错误＃要包含在跟踪中的项目。
 
#METRICS EXPORT（MetricExportProperties）
spring.metrics.export.aggregate.key-pattern = ＃模式，告诉聚合器如何处理源存储库中的键。
spring.metrics.export.aggregate.prefix = ＃全局存储库的前缀（如果处于活动状态）。
spring.metrics.export.delay-millis = 5000 ＃导出刻度之间的延迟（以毫秒为单位）。根据此延迟，度量标准按计划导出到外部源。
spring.metrics.export.enabled = true ＃启用度量标准导出的标志（假设MetricWriter可用）。
spring.metrics.export.excludes = ＃要排除的度量标准名称的模式列表。包含后应用。
spring.metrics.export.includes = ＃要包括的度量标准名称的模式列表。
spring.metrics.export.redis.key = keys.spring.metrics #Redis 存储库导出的密钥（如果处于活动状态）。
spring.metrics.export.redis.prefix = spring.metrics #Redis 存储库的前缀（如果处于活动状态）。
spring.metrics.export.send-latest = #Flag 用于根据未导出未更改的度量标准值关闭任何可用的优化。
spring.metrics.export.statsd.host = #stats服务器的主机，用于接收导出的指标。
spring.metrics.export.statsd.port = 8125 ＃statsd服务器的端口，用于接收导出的指标。
spring.metrics.export.statsd.prefix = #statss导出指标的前缀。
spring.metrics.export.triggers。* = ＃每个MetricWriter bean名称的特定触发器属性。
 
 
# ----------------------------------------
#DEVTOOLS PROPERTIES
# ----------------------------------------
 
#DEVTOOLS（DevToolsProperties）
spring.devtools.livereload.enabled = true ＃启用livereload.com兼容服务器。
spring.devtools.livereload.port = 35729 ＃服务器端口。
spring.devtools.restart.additional-exclude = ＃应该从触发完全重启中排除的其他模式。
spring.devtools.restart.additional-paths = ＃要监视更改的其他路径。
spring.devtools.restart.enabled = true ＃启用自动重启。
spring.devtools.restart.exclude = META-INF / maven / **，META-INF / resources / **，资源/ **，静态/ **，公共/ **，模板/ **，** / * Test.class，** / * Tests.class，git.properties ＃应该从触发完全重启中排除的模式。
spring.devtools.restart.poll-interval = 1000 ＃轮询类路径更改之间等待的时间（以毫秒为单位）。
spring.devtools.restart.quiet-period = 400 ＃触发重启之前没有任何类路径更改所需的静默时间（以毫秒为单位）。
spring.devtools.restart.trigger-file = ＃更改后的特定文件的名称将触发重新启动检查。如果未指定任何类路径文件更改将触发重新启动。
 
#DROTE DEVTOOLS（RemoteDevToolsProperties）
spring.devtools.remote.context-path = /。~~ spring-boot！〜＃用于处理远程连接的上下文路径。
spring.devtools.remote.debug.enabled = true ＃启用远程调试支持。
spring.devtools.remote.debug.local-port = 8000 ＃本地远程调试服务器端口。
spring.devtools.remote.proxy.host = ＃用于连接远程应用程序的代理主机。
spring.devtools.remote.proxy.port = ＃用于连接远程应用程序的代理端口。
spring.devtools.remote.restart.enabled = true ＃启用远程重启。
spring.devtools.remote.secret = ＃建立连接所需的共享密钥（启用远程支持所需）。
spring.devtools.remote.secret-header-name = X-AUTH-TOKEN ＃用于传输共享密钥的HTTP头。
 
 
# ----------------------------------------
#TESTING PROPERTIES
# ----------------------------------------
 
spring.test.database.replace = any ＃要替换的现有DataSource的类型。
spring.test.mockmvc.print =默认#MVC 打印选项。

```



