
---
## SwiftDate概况

从swift发布起，我们就使用swift并喜欢swift。

当然，我们也希望我们能够轻松自如地管理日期和时区。这也是我们创建SwiftDate这个类库的原因，为的是在swift里面更加优雅地处理时间。

在iOS, macOS, watchOS, tvOS上，以及Swift兼容的平台上（Linux）都能完美运行！

此外，这个类库是免费的，开源的！

### 最新发布版本

最新版本是4.0.3（Swift3)
最新更新时间：2016-10-03
更新日志：[Read CHANGELOG](https://github.com/malcommac/SwiftDate/blob/master/CHANGELOG.md)

[获取最新版本](https://github.com/malcommac/SwiftDate)

### 老版本

如果你使用的是swift2.2或者swift2.3，你可以到[GitHub page](GitHub page)

* [Swift2.3分支](https://github.com/malcommac/SwiftDate/tree/feature/swift_23)
* [Swift2.2分支](https://github.com/malcommac/SwiftDate)


## 主要特点

这部分内容是swiftdate里面主要特点的一大亮点。

* 使用日期进行简单数学运算！例子: `aDate + 2.weeks + 1.hour or (1.year - 2.hours + 16.minutes).fromNow()`
* 时区，地区和日历的转换。使用类`DateInRegion`,通过组件和操作符进行转化。
* 数学比较运算进行时间比较。比如，`aDate1 >= aDate2` 或者 `aDate1.isIn(anotherDate, .day)`
* 使用时间组成元素。比如，使用你喜欢的时区格式表述 `aDateInRegion.day` 或 `hour`, `minutes`等等，
* 简单最佳的方式进行时间和字符串之间的转换。支持自定义(可读的)和固定格式(ISO8601, AltRSS, RSS, Extended, .NET和一些按照unicode标准的常规字符串)。
* 用其他时间单位表述一个时间段。比如`120.seconds.in(.minutes) // 2 minutes`
* 操作时间单位、间隔和常见操作日期，获取时间间隔的便捷之道。(`isYesterday`,`isTomorrow`,`isBefore()`...)
* ...更多令人激动的事情。


## 环境要求

目前官方的版本是v4，一些要求：

* Swift 3.0+
* iOS 8 or later
* macOS 10.10 or later
* watchOS 2.0 or later
* tvOS 9.0 or later
* ...任意安装Swift3以及Swift的基本库的平台


## 安装

SwiftDate支持多种安装方式。

### CocoaPods安装方式

CocoaPods是一个Objective-C和Swift的依赖管理，在项目中能够自动简洁加入使用第三方的类库。

安装CocoaPods可以使用下面的命令：

`$ gem install cocoapods`

SwiftDate 4.+的版本需要使用CocoaPods 1.0.1+。

#### Podfile

在Xcode项目中使用CocoaPods引入SwiftDate，只需要在Podfile中新增：
```
source 'https://github.com/CocoaPods/Specs.git'
platform :ios, '8.0'

target 'TargetName' do
pod 'SwiftDate', '~> 4.0'
end
```

### Carthage安装方式

Carthage是一种非集成的依赖管理器，构建依赖，并提供二元框架。

你可以使用homebrew安装Carthage

```
$ brew update
$ brew install carthage
```

在Xcode项目中使用Carthage引入SwiftDate，只需要在Cartfile中新增：

```
github "malcommac/SwiftDate" ~> 4.0
```


### Swift Package Manager安装

目前还不支持！


## Fork us on GitHub

SwiftDate是开源的类库，托管在GitHub上。

如果你想为SwiftDate作出贡献，你可以尝试下面的方式：

* 如果你发现了一个bug，并且能提供详细步骤并复现bug，你可以open一个issue。
* 如果你有一个特定的要求，你可以open一个issue。
* 如果你想贡献代码，你可以提交pr。

## Authors & License

SwiftDate是由[Daniele Margutti](http://www.danielemargutti.com/)创建并维护，其中项目的一个主要贡献者是[Jeroen Houtzager](https://github.com/Hout)。

欢迎为开源项目作出贡献！

此类库的源代码遵循[MIT License](https://github.com/malcommac/SwiftDate/blob/master/LICENSE), 你可以没有任何限制地在商业项目中使用！

唯一的要求就是增加一行说明：

```
Date and Time Management is provided by SwiftDate - http://www.swift-date.com
Created by Daniele Margutti and licensed under MIT License.
```


## Your App & SwiftDate

如果你有兴趣，可以整理出使用SwiftDate这个类库的项目。可以在GitHub上开一个issue，提供你的项目名字和链接，我们将会添加到本网站上！








