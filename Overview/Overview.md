
---
## SwiftDate概况

从Swift发布起，我们就没有放弃使用Swift。

当然，我们希望在项目能够轻松自如地管理日期和时区，所以创建`SwiftDate`这个类库。有了“她”在Swift里面优雅地处理时间。

在iOS、macOS、watchOS、tvOS上，以及Swift兼容的平台上（Linux）都能完美运行！

此外，这个类库是免费的，开源的！

### 最新发布版本

最新版本是4.0.3（Swift3)
最新更新时间：2016-10-03
更新日志：[Read CHANGELOG](https://github.com/malcommac/SwiftDate/blob/master/CHANGELOG.md)

[获取最新版本](https://github.com/malcommac/SwiftDate)

### 老版本

如果你使用的是swift2.2或者swift2.3，你可以到[GitHub page](https://github.com/malcommac/SwiftDate)

* [Swift2.3分支](https://github.com/malcommac/SwiftDate/tree/feature/swift_23)
* [Swift2.2分支](https://github.com/malcommac/SwiftDate)


## 主要特点

这部分内容是swiftdate里面主要特点的一大亮点。

* 日期进行简单数学运算。例如: `aDate + 2.weeks + 1.hour or (1.year - 2.hours + 16.minutes).fromNow()`
* 时区，地区和日历的转换。使用类`DateInRegion`,通过组件和操作符进行转化。
* 算术比较运算比较时间。例如，`aDate1 >= aDate2` 或者 `aDate1.isIn(anotherDate, .day)`
* 使用时间组件。比如，用你喜欢的时区格式表述 `aDateInRegion.day` 或 `hour`, `minutes`等等，
* 最优雅的方式进行时间和字符串之间的转换。支持自定义(可读的)和固定格式(ISO8601, AltRSS, RSS, Extended, .NET和一些按照unicode标准的常规字符串)。
* 用其他时间单位描述一个时间段。比如`120.seconds.in(.minutes) // 2 minutes`
* 快捷获取时间和时间间隔。(`isYesterday`,`isTomorrow`,`isBefore()`...)
* ...更多令人激动的事情！


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

CocoaPods是一个Objective-C和Swift的依赖管理器。

安装CocoaPods命令：

```
$ gem install cocoapods
```

SwiftDate 4.+的版本需要使用CocoaPods 1.0.1+。

#### Podfile文件

在Xcode项目中引入SwiftDate，编辑Podfile新增：
```
source 'https://github.com/CocoaPods/Specs.git'
platform :ios, '8.0'

target 'TargetName' do
pod 'SwiftDate', '~> 4.0'
end
```

### Carthage安装方式

Carthage是一种非集成的依赖管理器，构建依赖，并提供二元框架。

homebrew安装`Carthage`：

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

SwiftDate是开源的类库，源码托管在GitHub上。

👇下面的姿势可以为SwiftDate作贡献：

* 抓到一个bug，提供详细步骤复现bug，open一个issue。
* 提出一个功能性的请求，open一个issue。
* 贡献代码，提交pr。
* ...

## Authors & License

SwiftDate是由[Daniele Margutti](http://www.danielemargutti.com/)创建并维护，其中项目的一个主要贡献者是[Jeroen Houtzager](https://github.com/Hout)。

欢迎为开源项目作出贡献！

此库的源代码遵循[MIT License](https://github.com/malcommac/SwiftDate/blob/master/LICENSE), 你可以没有任何限制地在商业项目中使用！

唯一的要求就是增加一行说明：

```
Date and Time Management is provided by SwiftDate - http://www.swift-date.com
Created by Daniele Margutti and licensed under MIT License.
```


## Your App & SwiftDate

如果你有兴趣，可以整理出使用SwiftDate这个类库的项目。可以在GitHub上开一个issue，提供你的项目名字和链接，我们将会添加到本网站上！








