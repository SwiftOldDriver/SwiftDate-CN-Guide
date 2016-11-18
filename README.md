##SwiftDare 中文版说明文档 - 解析／创建日期 - 4
@(丁香园学习笔记)[swift, 翻译]

###概览
----
一个关联到具体地区的时间可以由多种方法创建；这种时间可以由一对 `Date` 和 `Region` 对象，或者从一个表示自定义时间格式（SwiftDate 支持自定义的时间格式，诸如 [ISO8601 标准格式](https://en.wikipedia.org/wiki/ISO_8601)，[RSS 或AltRSS](https://validator.w3.org/feed/docs/rss2.html) 和 [.NET 时间](https://msdn.microsoft.com/en-us/library/az4se3k1%28v=vs.110%29.aspx)）的字符串解析来创建，再或者通过解析 `Calendar.Component`对象集合来创建。
当然你也可以通过数学运算从另两个时间来新建时间。
本篇副罗列了所有关于创建时间的方法，这些方法对创建`DateInRegion` 和 `Date` 对象都适用。
  
    
###根据字符串解析时间
----
众所周知，解析字符串并转换成时间是个无聊的行为。SwiftDate 通过支持众多时间格式帮你提高效率。
你可以给 `format` 参数赋值说明你想要使用的使用的时间格式：可以是自定义时间格式字符串或其他广为人知的 ISO8601 datetime、.NET datetime 标准的时间格式字符串。

**声明**
`func init(string: String, format: DateFormat, fromRegion region: Region? = nil) throws`

**参数**
+ `string` : this is the string you want to parse
+ `format` :  this is the format in which you expect the string is formatted. `DateFormat` is an enum: `.custom` (for custom format), `.iso8601` to parse all available specs for ISO8601 DateTime Format, `.extended` to parse Extended DateTime format, `.rss` to parse both RSS and AltRSS datetime formats and .dotNET to parse .NET datetime strings.
+ `region` : is the region in which you want to express specified date. If nil or not specified Region.Local(( is used instead.

**返回结果**
返回结果是一个解析自给定地区的 `DateInRegion` 时间实例。 
**例子**
```
let rome = Region(tz: TimeZoneName.europeRome, cal: CalendarName.gregorian, loc: LocaleName.italian)

// 基于自定义时间格式解析时间字符串
let date1 = try! DateInRegion(string: "1999-12-31 23:30:00", format: .custom("yyyy-MM-dd HH:mm:ss"), fromRegion: regionRome)

// 基于 AltRss 标准来解析时间字符串
let date2 = try! "3 feb 2001 15:30:00 +0100".date(format: .rss(alt: true), fromRegion: regionRome)
// 同上
let date3 = try! DateInRegion(string: "3 feb 2001 15:30:00 +0100", format: .ss(alt: true)), fromRegion: regionRome)

//  解析 ISO8601 标准互联网时间字符串
let date4 = DateInRegion(string: "2001-02-03T15:30:00+01:00", format: .iso8601(options: .withInternetDateTime), fromRegion: regionRome)

// 解析自定义时间格式字符串
let date5 = try! DateInRegion(string: "sab 3 feb 2001, 30 minutes after 15 (timezone is +0100)", format: .custom("eee d MMM YYYY, m 'minutes after' HH '(timezone is' Z')'"), fromRegion: regionRome)
```

###创建当前时间
---
使用默认的 `init()` 方法是一种方便快捷的方法来创建基于设备当前地区的 `DateInRegion` 时间实例。

**声明**
`func init()`

**返回结果**
返回的 `DateInRegion` 对象定义了当前时刻（`Date()`）和设备当前的所在地区 此地区属性同时也定义了设备所在的时区（`Region.Local()`） `.timeZone`、区域  `.locale`、当地日历格式 `.calendar` （所有相关设置都会自动更新）

**例子**
```
// Create a new DateInRegion which represent the current moment (Date()) in current device's local settings
let now = DateInRegion()
```


###根据给定的时刻和地区来创建时间
---
你可以创建一个定义了时间和其所在地区的 `DateInRegion` 对象。一旦创建，使用新的 `DateInRegion` 对象进行的所有操作都将在对应地理区域中表示；`DateInRegion`对象的属性和方法会自动处理所有区域设置；
**声明**
`func init(absoluteDate date: Date, in region: Region)`
**参数**
+ ``date``: define the absolute `Date` you want to use to create the new `DateInRegion`. Passed date is indipendent from any geographic timezone/calendar or locale because it's expressed in absolute time.
+ ``region``: define the destination `Region` in which you want to express passed `date`

**返回结果**
返回对象是一个解析自给定地区的 `DateInRegion` 时间实例。 

**例子**

```
// Create a Region in Rome TimeZone with Gregorian Calendar and Italy locale settings
let regionRome = Region(tz: TimeZoneName.europeRome, cal: CalendarName.gregorian, loc: LocaleName.italianItaly)
// Resulting object is DateInRegion which express the current moment in Rome
let dateInRome = DateInRegion(absoluteDate: Date(), in: regionRome)
```

###根据日期要素创建时间
---

将日历的因素集合以 `DateComponents` 对象封装后创建 `DateInRegion` 时间是另一种好方法。`DateComponents` 实例化对象的`TimeZone` `Locale` `Calendar`  属性都必须声明以保证获得的时间有效；如果缺失任何一个，将会抛出 `.MissingCalTzOrLoc` 异常。

**声明**
`func init(components: DateComponents)`

**参数**
+ ``components``: components used to generate the new date

**返回结果**
返回一个 `DateInRegion` 时间实例，其日期由传入的 `DateComponets` 来决定；

**例子**

```
var cmp = DateComponents()
cmp.timeZone = TimeZoneName.europeOslo.timeZone
cmp.calendar = CalendarName.gregorian.calendar
cmp.calendar?.locale = LocaleName.englishNorway.locale
cmp.year = 2005
cmp.month = 4
cmp.day = 15
cmp.hour = 20
cmp.minute = 30

// create a new DateInRegion on 15 Apr 2005, 20:30:00 GMT+2
let date = try! DateInRegion(components: cmp)
```

###根据时间要素创建时间
---
可以通过传入一组 `Calendar.Component` 和时间相对值（由`[Calendar.Component:Int]` 样式的字典和具体的地区所定义）来创建一个新的 `DateInRegion` 时间对象
**声明**
``func init(components: [Calendar.Component:Int], in region: Region)``

**参数**
+ `components`: components used to generate the new date. It's a dictionary where keys are `Calendar.Component` and values are `Int` with relative value. Supported components are: `.day`,` .era`,` .hour`,` .minute`,` .month`,` .nanosecond`,` .quarter`,` .second`,` .weekOfMonth`,` .weekOfYear`,` .weekday`,` .weekdayOrdinal`,` .year`, `.yearForWeekOfYear`。
+ ``region``: is the region in which you want to express specified date. If nil or not specified Region.Local(( is used instead.

**返回结果**
返回一个 `DateInRegion` 时间实例，其日期由传入的 `DateComponets` 来决定；

**例子**

```
let c: [Calendar.Component : Int] = [.year: 2002, .month: 3, .hour: 5, .day: 4, .minute: 6, .second: 7, .nanosecond: 87654321]
// create a new DateInRegion on 2002-03-04 at 05:06:07.87654321 (+/-10) in Region.Local()
let date = try! DateInRegion(components: c, fromRegion: nil)
```
