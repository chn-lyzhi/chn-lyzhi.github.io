---
layout: post
title:  "iOS - CocoaPods pod install/pod update更新慢的问题"
date:   2015-01-19 15:56
categories: jekyll update
tags: iOS
---

最近使用CocoaPods来添加第三方类库，无论是执行pod install还是pod update都卡在了Analyzing dependencies不动

原因在于当执行以上两个命令的时候会升级CocoaPods的spec仓库，加一个参数可以省略这一步。加参数的命令如下：

`pod install --verbose --no-repo-update`
`pod update --verbose --no-repo-update`