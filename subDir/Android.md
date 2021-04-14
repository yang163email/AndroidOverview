## Android

### View相关

1. invalidate与requestLayout

   - invalidate只会触发draw方法。两种（启动硬件加速，以及不启动硬件加速）

     - 硬件加速绘制：只会绘制发生变化的区域
     - 软件绘制：会遍历整个view树进行绘制

   - requestLayout会触发measure、layout，如果view的尺寸发生变化，会触发invalidate，从而调用draw方法。

     

### 其他

1. Android 为每个应用程序分配的内存大小是多少？

   根据不同手机，分配的大小不尽相同。

   在AndroidMenifest文件中application标签上添加 largeHeap=true，可申请的内存会相应增大。

   这些值在 /system/build.prop文件中设置。