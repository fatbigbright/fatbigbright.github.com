---
layout: post
title: iOS开发笔记
permalink: ios-dev-notes
description: Some Description
date: 2013-03-14 09:40:02 +08:00
tags: "iOS dev"
---

###iOS开发笔记

####本开发笔记将不定时徐徐更新。

1. UITableView的单元格存在图片的情况下，在划动时会存在卡顿的现象。现有的优化方案有将源图改小保存一个复本，单元格显示这个较小的复本，或者使用异步加载，尚需试验确认。—— 实验结果，异步加载没能改善问题，造成卡顿的瓶颈并非在于图片的加载，而在于图片引用的绑定，而这一过程，是主线程做的，所以只能尝试修改源图的方案，实验结果表明有明显改善。

2. 如何下载XCode的安装包，而不是从Mac App Store上下载？ 访问[https://developer.apple.com/downloads/index.action](https://developer.apple.com/downloads/index.action)即可。

3. 如何让XCode 4和XCode 5共存？ 参考这篇[日语博文](http://dev.classmethod.jp/references/xcode-5-xcode-4/)，不过还未验证。