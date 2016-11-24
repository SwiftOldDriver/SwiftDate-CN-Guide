---

## 概况

在SwiftDate中使用时间的组件是相当的简单的。`DateInRegion`和`Date`都实现了同一组属性和函数来查看时间单位管理日期。

需要记住的是：当使用`Date`对象的时候，需要在`.defaultRegion`中进行`Date`的实例化。

此属性的初始值是`Region.GMT()`，这是定义位于GMT时间、当前设备的语言环境和日历的区域。

此外，还可以通过调用`Date`的静态方法`.setDefaultRegion()`改变默认的区域。


## era
返回era单位的数值
### 声明
`public var era: Int`

### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## year
返回years单位的数值
### 声明
`public var year: Int`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。


## month
返回months单位的数值
### 声明
`public var month: Int`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。


## day
返回days单位的数值
### 声明
`public var day: Int`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。


## hour
返回hour单位的数值
### 声明
`public var hour: Int`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。


## nearestHour
根据四舍五入的方法取出某个日期的最近小时。
### 声明
`public var nearestHour: Int`

### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。


## minute
返回minute单位的数值
### 声明
`public var minute: Int`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## second
返回second单位的数值
### 声明
`public var second: Int`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## nanosecond
返回nanosecond单位的数值
### 声明
`public var nanosecond: Int`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## yearForWeekOfYear
返回按周编号单位的数值
### 声明
`public var yearForWeekOfYear: Int`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## weekOfYear
返回一年的星期日期
### 声明
`public var weekOfYear: Int`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## weekday
返回工作日单位的数值。

工作日单位的数值是1-n，其中n是一个星期中的天数。

比如：在公历中，n是7，1代表星期天。
### 声明
`public var weekday: Int`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。


## weekdayOrdinal
返回工作日单位的顺序数值。

工作日顺序单位表示下一个较大日历单位（例如月份）内工作日的位置。

比如：2代表该月的第二个星期五的工作日序数单位。
### 声明
`public var weekdayOrdinal: Int`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## weekdayName
某个日期的weekday名称
### 声明
`public var weekdayName: String`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## monthDays
当前地区日历和语言环境中，当前月份的天数
### 声明
`public var monthDays: Int`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## quarter
返回季度单位的数值
### 声明
`public var quarter: Int`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## weekOfMonth
返回月份的周数
### 声明
`public var weekOfMonth: Int`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## shortMonthName
短名称的日期
### 声明
`public var monthName: Int`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## leapMonth
返回一个布尔值，说明某个月份是否是闰月。
如果返回true，次月份就是闰月，否则不是闰月。
### 声明
`public var leapMonth: Bool`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## leapYear
返回一个布尔值，说明某个年份是否是闰年。
如果返回true，次月份就是闰年，否则不是闰年。
### 声明
`public var leapYear: Bool`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。


## julianDay
儒略日是天文学家使用从朱利安时期以来连续的天数。
### 声明
`public var julianDay: Double`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## modifiedJulianDay
在1957年，史密森天体物理天文台通过IBM 704(36位)记录的人造卫星的轨道，直到2576年8月7日只使用18位介绍了修改后的朱利安日期(MJD)。
### 声明
`public var modifiedJulianDay: Double`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## previousWeekend
返回两个DateInRegion对象表示开始和结束日期的前一个周末。

两个DateInRegion对象表示的对象是一个开始和结束日期元组的前一个周末。

当接收器在一个周末之前，返回的不是当前的这个周末

### 声明
`public var previousWeekend: (startDate: DateInRegion, endDate: DateInRegion)?`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## thisWeekend
返回两个DateInRegion对象表示开始和结束当前的周末。

两个DateInRegion对象表示的对象是一个开始和结束当前元组的当前周末。

如果这是一个周末,则返回nil。

### 声明
`public var thisWeekend: (startDate: DateInRegion, endDate: DateInRegion)?
`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。


## nextWeekend
返回两个DateInRegion对象表示的开始和结束日期后的下个周末。

两个DateInRegion对象表示的对象是一个开始和结束日期元组的下个周末。

当接收器在一个周末时，返回的值是下一个周末不是当前周末。
### 声明
`public var nextWeekend: (startDate: DateInRegion, endDate: DateInRegion)?`

### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## isToday
返回布尔值，给定日期是否为当前天日期。
### 声明
`public var isToday: Bool`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## isYesterday
返回布尔值，给定日期是否为昨天的日期。
### 声明
`public var isYesterday: Bool`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## isTomorrow
返回布尔值，给定日期是否为明天的日期。
### 声明
`public var isTomorrow: Bool`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## isInWeekend
返回布尔值，给定日期是否为周末日期。
### 声明
`public var isInWeekend: Bool`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## isInPast
如果给定日期代表通过日期返回true。
### 声明
`public var isInPast: Bool`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## isInFuture
如果给定的日期代表未来的日期返回true
### 声明
`public var isInFuture: Bool`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## isInSameDayOf()
在接受器所选择的时区和日历中，返回给定日期是否在同一天。
### 声明
`public func isInSameDayOf(date: DateInRegion) -> Bool`
`public func isInSameDayOf(date: Date) -> Bool`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## startOfDay
从接收器选择的日历中给定一个日期，返回代表给定日期的第一时刻的实例。
### 声明
`public var startOfDay: DateInRegion`
`public var startOfDay: Date`

### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## endOfDay
从接收器选择的日历中给定一个日期，返回代表给定日期的最后时刻的实例。
### 声明
`public var endOfDay: DateInRegion`
`public var endOfDay: Date`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## nextMonth
返回某个日期加上一个月的日期
### 声明
`public var nextMonth: DateInRegion`
`public var nextMonth: Date`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。


## prevMonth
返回某个日期减去一个月的日期
### 声明
`public var prevMonth: DateInRegion `
`public var prevMonth: Date`
### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。

## startOf()
使用日期单位，并在该单位的开头返回日期。
### 声明
`public func startOf(component: Calendar.Component) -> DateInRegion`
`public func startOf(component: Calendar.Component) -> Date`
### 参数
* `component`: 时间单位组件作为参考

### 说明
这个值将会在其使用的日历和时区的环境中解释；如果调用者是`DateInRegion`，系统环境将会使用相关的`.region`来定义，如果调用者是普通`Date`，系统环境将会使用默认值`Date.defaultRegion`来定义。



