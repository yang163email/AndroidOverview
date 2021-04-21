## OkHttp

### 一、拦截器

1. 拦截器有哪些？分别有什么用处？

   - 自定义拦截器

     - 开发者可自行定义，比如请求头添加统一参数，数据解析自处理等

   - RetryAndFollowUpInterceptor

     - 主要是做一些请求失败的重试，以及重定向之后的后续请求。
     - 里面有一个while循环，需要重定向的时候会继续下一次请求。

   - BridgeInterceptor

     - 构建一个能够进行网络访问的请求，比如一些头部字段的添加。cookie在这里设置

   - CacheInterceptor

     - 可以设置网络缓存，传入cache来进行处理。

       如果本地有可用的cache，就可以在没有网络交互的情况下返回结果。
       
     - 存储于获取：

       1. 设置OkHttp配置项，通过一个DiskLRUCache来存储。
       2. 只能缓存 GET 请求，不是no-cache才能缓存

   - ConnectInterceptor

     - 先从连接池获取，拿不到就创建socket，并建立连接（TCP/TLS），还会创建负责编码解码的HttpCodeC

   - networkInterceptors

     - 开发者自定义，原始网络数据可以在这里看到。

   - CallServerInterceptor

     - 这里进行网络的请求与相应，即网络I/O操作，通过socket读写数据