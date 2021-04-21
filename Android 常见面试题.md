## Android 常见面试题

### Android

1. Activity相关
   - 四大启动模式，以及应用场景
   - 生命周期
     - 从 Activity A 跳转 Activity B, 然后返回，生命周期如何调用
     - 横竖屏切换生命周期变化
   - onSaveInstanceState 方法的作用？何时会被调用？
   - 常见的标记位 Flags?
   - 如何启动其他应用的 Activity？
2. 广播
   - 广播有哪几种
   - 静态注册于动态注册的区别
3. 屏幕适配方案以及原理
4. Handler机制。
   - Looper死循环为什么不会阻塞主线程（造成ANR），底层用到哪些机制。
5. IdleHandler
6. View相关
   - 事件分发机制
   - 绘制原理（measure/layout/draw）
   - invalidate/requestLayout/postInvalidate区别
   - 自定义View有哪几种方式。
   - 竖向 TextView 实现？
   - ACTION_CANCEL 事件何时触发？
7. Bitmap
   - 内存计算方式
   - 高效加载
8. Binder
   - Binder特点以及原理，与其他IPC方式有哪些优缺点。
   - 空间大小
   - AIDL做了哪些工作
9. 序列化方式，区别（Serialzable /Parcelable）
10. APP的启动过程
11. Activity启动过程
12. Apk安装过程
13. Activity、Window、ViewRoot、DecorView关系
14. Context的理解
15. 动画
    - 有哪些动画
    - 属性动画与 View 动画区别
16. RecyclerView源码分析
17. Android 各版本特性（一般是适配到的最新版本）
18. 签名机制
19. SharedPrefences 的 commit 与 apply 的区别？为什么会导致ANR？
20. HandlerThread
21. LinearLayout、RelativeLayout、FrameLayout的性能
22. Android中的集合框架
    - ArrayMap
23. 数据库
    - 升级时需要新增、删除、修改字段时，怎么操作？
24. Android 中进程的优先级？
25. Android 为每个应用程序分配的内存大小是多少？

### Java

1. equals与==的区别？equals与hashcode的关系
2. String、StringBuffer、StringBuilder的区别
3. 面向对象三大特点（封装、继承、多态）
4. 抽象类与接口的特点
5. 集合
   - ArrayList、CopyOnWriteArrayList、LinkedList原理
   - HashMap特点，原理，扩容 机制，hash算法以及计算桶的位置
   - ConcurrentHashMap原理，sizeCtl含义
6. 泛型
   - 泛型理解
   - 泛型擦除
7. 线程
   - 线程状态
   - wait与sleep区别
   - 线程与进程的区别
8. 线程池
   - 与线程相比，其特点
   - 线程池几个参数对应的意思，线程池类型
   - 拒绝执行策略有哪几种
   - 线程池的工作流程
9. 锁
   - 死锁触发条件，如何解决
   - synchronized用法？放入对象与Class的区别？
   - synchronized的原理，修饰方法或者代码块时字节码方面的变化
   - synchronized与Lock的区别
   - 乐观锁、悲观锁
   - CAS是什么，底层原理，ABA问题，如何解决
   - 公平锁、非公平锁
   - 无锁、偏向锁、轻量级锁、重量级锁
   - 可重入锁、不可重入锁
   - 独享锁、共享锁
10. 线程间通信
    - notify与notifyAll的区别
    - wait/notify和Condition类实现的等待通知有什么区别
11. 多线程
    - 原子性、可见性、有序性分别代表什么意思
    - volatile 原理
    - ThreadLocal

### JVM

1. 内存模型
   - 内存区域划分
   - Java对象创建过程
2. GC机制
   - 可当做GC Roots的对象
   - GC的常用算法
   - Minar GC 与 Full GC的区别
   - 四种引用区别
   - 新生代与老年代，新生代回收多少次会移到老年代？
3. 类加载
   - 类的加载过程
   - 类加载机制，双亲委派机制
   - 类加载器

### Kotlin

1. ==、=== 和 equals 的区别
2. 高阶函数
3. 协程是什么？原理？

### 网络

1. HTTP
   - 常见状态码
   - HTTP 1.1 与 HTTP 2 区别
   - HTTP/HTTPS 两者区别
   - HTTPS 加密过程
2. TCP
   - 三次握手
   - 四次挥手
   - TCP 与 UDP 的区别
   - TCP 流量控制与拥塞控制

### 设计模式

1. 六大原则
2. 单例模式
   - 几种实现方式
   - DCL 模式会出现的问题
3. 观察者模式
4. 代理模式
5. 装饰者模式
6. 责任链模式
7. 建造者模式

### 架构设计

1. MVC
2. MVP
   - MVC 与 MVP 的区别
   - P层过大有哪些结局方式
3. MVVM
   - MVVM 与 MVP 的区别
   - 优点、缺点

### 开源框架

1. OkHttp
   - 责任链模式
   - 拦截器，有哪些，有什么功能
   - 里面有几个队列，默认线程池的具体情况
   - 连接池（复用Socket）
2. Retrofit
   
   - 涉及的技术点（注解、动态代理）
3. LeakCanary
   
   - 原理
4. ViewModel与LiveData

   - 原理，需不需要手动解除观察（或者为什么会感应到生命周期变化）

   - LiveData里面 postValue 会有什么问题？

     提示：可能会出现只执行最后一个发送消息的情况
5. Glide
   - 加载优化（Bitmap加载）
   - 缓存机制
   - 生命周期处理

### 性能优化

1. 布局优化
2. 绘制优化
   - 前因后果
   - 分析工具（Systrace）
   - Systrace 里面内容（线程状态对应颜色、Flinger颜色对应状态）
3. 内存优化
   - 内存泄漏分析工具，分析过程
   - 造成内存泄漏的原因
   - OOM产生的原因，解决方式
4. 启动速度优化
5. 包体积优化
6. 电量优化
   - 哪些操作是耗电大户
   - 工具Battery Historian
7. ANR
   - 产生的原因，如何避免
   - 哪些情况会造成，出现后如何分析

### 算法

1. 16进制转10进制
2. 链表相关（链表反转、链表合并等）
3. 二叉树相关
4. 排序相关
5. 设计LRU

