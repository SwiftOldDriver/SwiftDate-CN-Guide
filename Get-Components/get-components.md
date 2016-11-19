---

## 概况

在SwiftDate中使用时间的组件是相当的简单的。`DateInRegion`和`Date`都实现了同一组属性和函数来查看时间单位管理日期。

需要记住的是：当使用`Date`对象的时候，需要在`.defaultRegion`中进行`Date`的实例化。

此属性的初始值是`Region.GMT()`，这是定义位于GMT时间、当前设备的语言环境和日历的区域。

此外，还可以通过调用`Date`的静态方法`.setDefaultRegion()`改变默认的区域。


## era（世纪）
给接收者era单位的数值
### 声明
`public var era: Int`

### 说明
在其使用的日历和时区的上下文中将会解释此值

## year（年）
给接收者years单位的数值
### 声明
`public var year: Int`
### 说明


## month（月）
给接收者months单位的数值
### 声明
`public var month: Int`
### 说明


## day（日）
给接收者days单位的数值
### 声明
`public var day: Int`
### 说明




## hour（小时）
给接收者hour单位的数值
### 声明
`public var hour: Int`
### 说明



## nearestHour（最近的小时）
根据四舍五入的方法取出某个日期的最近小时。
### 声明
`public var nearestHour: Int`

### 说明



## minute（分）
给接收者minute单位的数值
### 声明
`public var minute: Int`
### 说明



## second（秒）
给接收者second单位的数值
### 声明
`public var second: Int`
### 说明



## nanosecond（纳秒）
给接收者nanosecond单位的数值
### 声明
`public var nanosecond: Int`
### 说明


## yearForWeekOfYear
给接收者按周编号单位的数值
### 声明
`public var yearForWeekOfYear: Int`
### 说明

## weekOfYear
给接收者一年的星期日期
### 声明
`public var weekOfYear: Int`
### 说明


## weekday（工作日）
给接收者工作日单位的数值。

工作日单位的数值是1-n，其中n是一个星期中的天数。

比如：在公历中，n是7，1代表星期天。
### 声明
`public var weekday: Int`
### 说明


## weekdayOrdinal
给接收者工作日单位的顺序数值。

工作日顺序单位表示下一个较大日历单位（例如月份）内工作日的位置。

比如：2代表该月的第二个星期五的工作日序数单位。
### 声明
`public var weekdayOrdinal: Int`
### 说明


## weekdayName
某个日期的weekday名称
### 声明
`public var weekdayName: String`
### 说明



## endOfDay

### 声明

### 说明

## nextMonth
返回某个日期加上一个月的日期
### 声明
`public var nextMonth: DateInRegion`
`public var nextMonth: Date`
### 说明


## prevMonth
返回某个日期减去一个月的日期
### 声明
`public var prevMonth: DateInRegion `
`public var prevMonth: Date`
### 说明


## startOf()
使用日期单位，并在该单位的开头返回日期。
### 声明
`public func startOf(component: Calendar.Component) -> DateInRegion`
`public func startOf(component: Calendar.Component) -> Date`
### 参数
* `component`: 时间单位组件作为参考
### 说明



