
---

## Date 和 Absolute Time

Date是日期和时间处理类的基础。

这个类库封装了从2001年1月1日00:00 UTC以来作为秒数内部存储的时刻。

普遍认为，世界各地都处于相同的时间(除非新的星系日期系统出现才会改变)。

你可以认为绝对时间是这样一种概念：在某个时刻，美国的某个人正在跟在迪拜的某个人通电话；在同一时刻都会有这样的通话，但是由于时区、日历以及字母符号不相同的问题，当地时间就可能不一样。

基础库还支持日历对象：它允许我们处理不同的情况下的日期。

在处理跨时区、日历和语言环境的时间转换的时候，SwiftDate能够帮助我们解决这些问题。

## DateInRegion和Region

SwiftDate为了提供完整的时间和日期管理的功能，引入了两个重要的新对象和其他几个扩展。

第一个对象是一个结构体(struct)，称为Region：region，正如命名的那样，是地理学地区的一个命名，其中包含三个不同的特征：
> `TimeZone`: 用来定义时区对象。时区对象代表地域性的地区。也就是说，这些对象是用来命名地区的，时区对象还表示针对于格林威治标准时间GMT(Greenwich Mean Time)和太平洋标准时间PST(Pacific Standard Time)时间偏移量进行加减操作。 
> `Calendar`: 封装了关于计算时间的信息的信息，其中定义了年的开始、长度和年份的分割。提供了日历的信息，还支持日历的计算，例如确定给定的日历单元的范围以及给绝对时间添加单位。
> `local`: 关于语言学的、文化学的和科技的规矩和标准的信息概括。由一个区域设置封装的信息包括用于数字的小数点分隔符和日期格式的方式象征。

另外一个对象是DateInRegion。这个对象的主要目的是描述一个`Date`(与时区、日历没有一点关系)，还可以用`Region`描述：事实上，使用`DateInRegion`可以操作在特定上下文中定义的日期.


在SwiftDate中，你可以使用`DateInRegion`和`Date`管理时间，他们共有相同的函数和属性。


## 默认Region

你可能会注意到，当你使用普通的Date对象，你可以使用`Date.defaultRegion`中定义的DateInRegion，这个地区包含了：

* .timeZone 设置为GMT (Greenwich Mean Time)
* .local  设置为设备默认的地区
* .Calendar 设置为设备默认的日历

你可以调用函数 `Date.setDefaultRegion(:)` 随时随地的改变 `Date.defaultRegion` 。

请记住：这些需要在应用启动的时候设置（比如，iOS应用在UIApplication的delegate中函数`applicationDidFinishLaunching()`中设置就行了）。


