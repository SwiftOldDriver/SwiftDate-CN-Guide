
---

## Date 和 Absolute Time

`Date`是日期和时间处理类库的基础。这个类库封装了从2001年1月1日00:00 UTC以来作为秒数内部存储的时刻。

世界各地都处于同一个时间系(除非新的星系日期系统出现才会改变)。

绝对时间一种通俗的概念：在美国的A正在跟在迪拜的B进行通电话，这个时刻就可以称为绝对时间；在同一时刻都会有这样的通话，但是由于时区、不用的日历以及不同的字母或符号方法，区域时间就可能不一样。

基础库还支持`Calendar`对象：允许处理这些不同的情况。

在处理跨时区、日历和区域的时间转换的时候，都会遇到一些棘手的问题。SwiftDate能够解决这些问题。

## DateInRegion和Region

SwiftDate为了提供完整的时间和日期管理的功能，引入了两个重要的新对象和其他几个扩展。

第一个对象是一个结构体(struct)，称为Region：region，正如命名的那样，是地理学地区的一个命名，其中包含三个不同的特征：

#### 这或许是不太重要的标注说明：
> GMT(Greenwich Mean Time)：指格林威治标准时间；
> PST(Pacific Standard Time)：指太平洋标准时间；

* `TimeZone`: 用来定义时区对象。时区对象代表地域性的地区。也就是说，这些对象是用来命名地区的，时区对象还可以针对于GMT和PST时间的偏移量进行加减操作。 

* `Calendar`: 关于计算时间的信息概括，其中定义了年的开始、长度和年份的划分。提供了日历的信息，还支持日历的计算，例如确定某个给定的日历单元的范围以及给某个绝对时间添加单位。

* `local`: 关于语言学的、文化学的和科技的规矩和标准的信息概括。由一个区域设置封装的信息包含用于数字的小数点分隔符和日期格式的方式象征。

另一个对象是`DateInRegion`。此对象的主要目的是描述一个`Date`(与时区、日历没有一点关系)，还可以用`Region`描述：事实上，使用`DateInRegion`可以操作在特定上下文中定义的日期。


在SwiftDate中，可以使用`DateInRegion`和`Date`管理时间，他们共有相同的函数和属性。


## 默认Region

当你使用普通的`Date`对象，你可以在`Date.defaultRegion`中定义的DateInRegion，这个地区包含了：

* .timeZone 设置为GMT (Greenwich Mean Time)
* .local  设置为设备默认的地区
* .Calendar 设置为设备默认的日历

调用函数 `Date.setDefaultRegion(:)` 可以改变 `Date.defaultRegion` 。

这个或许不太重要但还是要记住：这些需要在应用启动前设置好（例如，在UIApplication的delegate中函数`applicationDidFinishLaunching()`中设置就行了）。


