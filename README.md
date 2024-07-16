# HTTP3
QUIC，HTTP3，SSE，HTTP3 PUSH，JAVA QUIC，Webtransport，Websocket

# QUIC&HTTP3
1. quic在线测试网站 https://http3.wcode.net/
2. 深入剖析HTTP3协议 https://www.taohui.tech/2021/02/04/网络协议/深入剖析HTTP3协议/
3. 深入剖析HTTP3协议 https://www.4hou.com/posts/wgxw
4. https://zhuanlan.zhihu.com/p/143464334
5. 与nginx的对比：https://www.banzhuti.com/openlitespeed-vs-nginx-2023.html
6. 各quic库 互操作性测试：https://interop.seemann.io/
7. python 的 quic /http3/websocket/webtransport https://github.com/aiortc/aioquic
8. HTTP3 RFC：https://www.rfc-editor.org/rfc/rfc9114.html#server-push
9. https://httpwg.org/specs/
10. QUIC RFC：https://github.com/quicwg/base-drafts
11. 有说法cloudflare 不会支持push：https://news.ycombinator.com/item?id=31648565


# SSE（因基于http3的webtransport不成熟，需要服务端PUSH PROMISE模式，可考虑SSE协议）
1. https://chromium.googlesource.com/chromium/blink/+/master/Source/core/page/EventSource.cpp#108
2. https://www.ruanyifeng.com/blog/2017/05/server-sent_events.html
3. https://dev.to/tjindapitak/server-sent-events-explained-2fd7
4. https://developer.mozilla.org/en-US/docs/Web/API/Server-sent_events/Using_server-sent_events#fields
5. https://textslashplain.com/2019/12/04/the-pitfalls-of-eventsource-over-http-1-1/
6. https://html.spec.whatwg.org/multipage/server-sent-events.html#server-sent-events
7. SSE的go的demo程序 ：https://github.com/r3labs/sse

# QUIC协议在Java中的应用
1. 在Java中，你可以使用quic-go库来实现QUIC协议。quic-go是一个基于Go语言的QUIC库，可以在Java中使用通过GraalVM的Native Image工具进行编译和运行。
2. 以下是在Java中使用quic-go库实现QUIC协议的一般步骤：
安装GraalVM和Native Image工具。你可以从Oracle官方网站上下载GraalVM和Native Image工具，并按照官方文档进行安装和配置。
安装quic-go库。你可以使用go get命令来安装quic-go库：go get -u gopkg.in/lucas-clemente/quic-go.v4
创建一个Java项目，并在项目中引入quic-go库的依赖。你可以在项目的构建文件（如Maven或Gradle）中添加quic-go库的依赖项。
在Java代码中使用quic-go库实现QUIC协议。你可以使用quic-go库提供的API来创建QUIC连接、发送和接收数据等操作。具体的代码实现可以参考quic-go库的文档和示例代码。
使用Native Image工具将Java项目打包成可执行文件。你可以使用Native Image工具的命令行界面或通过构建脚本（如Maven或Gradle）来执行此操作。Native Image工具将把Java项目和依赖项打包成一个可执行文件，这样可以减少程序的大小并提高运行效率。
除了使用quic-go库之外，Java中还有其他几种实现QUIC协议的方法：

使用第三方库：有一些第三方库提供了Java实现的QUIC协议，例如quic-api和quic-j等。这些库提供了QUIC协议的Java接口和实现，可以方便地在Java项目中使用。
使用JNI（Java Native Interface）：如果你对QUIC协议的实现细节比较了解，并且有一定的C/C++编程经验，你可以使用JNI在Java中调用C/C++实现的QUIC库。这样可以让你更灵活地控制QUIC协议的实现，但需要付出更多的开发时间和精力。
使用Java原生库：在Java中，你也可以使用Java原生库来处理QUIC协议。例如，你可以使用Java的javax.net.ssl包来实现QUIC协议的加密和认证功能。不过，这种方法可能需要你深入了解Java原生库和QUIC协议的实现细节。
需要注意的是，由于QUIC协议是一种相对较新的传输协议，因此其标准和实现仍在不断发展和完善中。在将QUIC协议应用于实际应用程序之前，建议仔细评估其适用性和稳定性，并进行充分的测试和验证。
                        
原文链接：https://blog.csdn.net/zhangzehai2234/article/details/134453688
