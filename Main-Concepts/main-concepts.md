
---

## Date 和 Absolute Time

Date是日期和时间处理类的基础。

在这个类库里面封装了一个从2001年1月1日00:00开始的时间片刻。

普遍认为，全世界到处都处于相同的时间(至少等到新的星系日期系统成为现实才会改变)。

你可以认为绝对时间是这样一种概念：在某个时刻，美国的某个人正在跟在迪拜的某个人通电话；在同一时刻都会有这样的通话，但是由于时区、不同的日历、不同的字母符号的问题，当地时间就可能不一样。

这就是基础库支持日历对象的原因：它允许我们处理这些不同的情况下的日期。

当程序员在处理跨时区、日历和语言环境的时间转换的时候，SwiftDate能够帮助我们解决这些问题。

## DateInRegion和Region

SwiftDate为了提供完整的管理时间和日期的功能，引入了两个重要的新对象和其他几个扩展。

第一个对象是一个结构体(struct)，称为Region：region，正如命名的那样，是地理学地区的一个命名，其中包含三个不同的特征：
> TimeZone: 定义时区对象的行为。时区对象代表地域性的地区。也就是说，这些对象是用来命名地区的，时区对象同时还代表着针对于GMT(Greenwich Mean Time)和PST(Pacific Standard Time)时间的漂移量。
> Calendar: 
> local: 关于语言学的、文化学的和科技的规矩和标准的信息概括。由一个区域设置封装的信息包括用于数字的小数点分隔符和日期格式的方式象征。

另外一个对象是DateInRegion。这个对象的主要目的是表述一个`Date`(跟特定的时区，日历没有一点关系)，还可以在一个区域中使用：这样的话，就可以操纵在一个特定的语境中定义的日期。

在SwiftDate中，你可以使用`DateInRegion`和`Date`管理时间，他们共有相同的函数和属性。


## 默认Region

你可能会注意到，当你使用普通的Date对象，你可以使用`Date.defaultRegion`中定义的DateInRegion，这个地区包含了：

* .timeZone 设置为GMT (Greenwich Mean Time)
* .local  设置为设备默认的
* .Calendar 设置为设备默认的

你可以使用函数 `Date.setDefaultRegion(:)` 随时随地的改变 `Date.defaultRegion` 。

请记住：这些需要在应用启动的时候设置（比如，iOS应用在UIApplication的delegate中函数`applicationDidFinishLaunching()`中设置就行了）。


