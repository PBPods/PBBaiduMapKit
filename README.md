# PBBaiduMapKit

官方地址 https://lbsyun.baidu.com

## 为什么不用官方的

1. <s>官方 pod 不包含 bitcode，而且官方站也找不到 bitcode 版的历史版本下载；</s>（4.2.0 起都是 bitcode 的了）；
2. 官方 pod 下载源设置的是 git 拉取 https://github.com/BaiduLBS/BaiduMapKit.git ，这样对网络要求比较高；二进制分发正确的做法是打压缩包放在自己的 CDN 上，要比从 GitHub 用 git 同步稳定、快速得多；
3. 官方 pod 强制导入自己的 OpenSSL，如果你的项目其他部分涉及到 OpenSSL 的使用可能会比较麻烦；正确的做法是提供建议并让用户自己决定如何导入第三方的东西；
4. 4.2.0 后增加了 WalkNavi，但组织完全不适合 CocoaPods，暂时通过增加 subspecs 解决。

## 其他修改

1. 修正了 header 不当的定义，它们在更严格的警告设置下会产生很多警告；
2. 素材资源包修改了我的位置的图片，SDK 虽然有 API 可以修改我的位置样式，但脑残的设定资源需要在 mapapi.bundle；
3. 素材资源包中移除了 @1x 的图片，并压缩了图片体积；
4. 素材资源包中百度 logo 去掉了。

## 使用

```ruby
source 'https://github.com/PBPods/PBBaiduMapKit.git'
pod 'PBBaiduMapKit', '~> 4.2'

# 百度用的 1.0 版本的 OpenSSL
source 'https://github.com/PBPods/PBOpenSSL.git'
pod 'openssl', '~> 1.0.0'
```
