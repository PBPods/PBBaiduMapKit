# PBBaiduMapKit

官方地址 https://lbsyun.baidu.com

## 为什么不用官方的

1. 官方 pod 不包含 bitcode；
2. 官方 pod 下载源设置的是 git 拉取 https://github.com/BaiduLBS/BaiduMapKit.git ，二进制分发应当打包放在自己的 CDN 上，要比从 GitHub 用 git 同步稳定、快速得多；
3. 官方站居然找不到 bitcode 版本的历史下载……自己保存历史版本吧。

## 其他修改

1. 修正了 header 不当的定义，它们在更严格的警告设置下会产生很多警告；
2. 资源包修改了我的位置的素材，百度 logo 去掉了。
