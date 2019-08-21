# CombineX([中文](README.zh_cn.md))

![travis](https://img.shields.io/travis/luoxiu/CombineX.svg)
![release](https://img.shields.io/github/release-pre/luoxiu/combinex)
![install](https://img.shields.io/badge/install-spm%20%7C%20cocoapods%20%7C%20carthage-ff69b4)
![platform](https://img.shields.io/badge/platform-ios%20%7C%20macos%20%7C%20watchos%20%7C%20tvos%20%7C%20linux-lightgrey)
![GitHub](https://img.shields.io/github/license/luoxiu/combinex?color=black)

CombineX is an open source implementation for Apple's [Combine](https://developer.apple.com/documentation/combine) specs. It allows you to use Combine's API right now, without the need for macOS 10.15 or iOS 13, without the need for the Apple platform.

## Status

Compatible with Combine beta 5. 

A new beta version will be released every Monday.

## Notice

This library is still in beta, **So do not use it in production.**

🐱

## Try it out

#### CocoaPods

In your `Podfile`:

```ruby
pod 'CombineX.swift', :git => 'https://github.com/luoxiu/CombineX.git', :branch => 'master'
```

#### Swift Package Manager

In your `Package.swift`:

```swift
pkg.dependencies.append(
    .package(url: "https://github.com/luoxiu/CombineX", ._branchItem("master"))
)
```

## Related

- [CombineX.Foundation](https://github.com/luoxiu/CombineX.Foundation): provides all `Foundation` extension implementations, built on top of `CombineX`, such as `URLSession`, `NotificationCenter`, `Timer`, etc.
- [CombineX.Cocoa](https://github.com/luoxiu/CombineX.Foundation): provides `Cocoa` exensions, built on top of `CombineX`.
- [CombineX.Compatible](https://github.com/CombineXCommunity/CombineX.Compatible): provides `CombineX` API Shims, help you resolve migration concerns that may arise.

## Contribute

Welcome! CombineX is always looking for collaborators! 

Now, what `CombineX` need most are testing. You can:

1. Add more functional tests.
2. Make sure `Combine` can pass it.
3. If `CombineX` can not pass it, open an issue, or fix it directly!

#### Flow

Since some people may not have macOS 10.15 beta installed, the recommended contributing way is: 

1. Fork the project.
2. Open `Specs/Specs.xcworkspace`, make your changes under `CombineX/CombineX` folder. 
3. All tests go `CombineXTests/CombineXTests` folder. Make sure both scheme `Specs` and scheme `CombineX` pass the tests you wrote.

## Bugs in Combine

Since `Combine` is still in beta, it is inevitable that it has bugs. If you find something strange, open an issue to discuss with us, or leave a `// FIXME:` annotation. In fact, there are already some `FIXME` annotations in `CombineX`.

## Other

#### Why write this?

1. `Combine` has a strict system version limit(macOS 10.15+, iOS 13+). This means that even if your app only needs to support two forward versions, you have to wait for almost three years.
2. `Combine` is closed source. It is the same as `UIKit`, `MapKit`, updating with the update of xcode. When you encounter a bug, you must have encountered a system library bug before, the debugging is very annoying. And the more annoying is the slow official response, usually you can only wait for the next regular update of xcode.
3. `Combine` is Apple platform only and doesn't support Linux.
