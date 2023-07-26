---
uid: 20230226222912
title: Cubox 通过 Advanced Uri 插件导入 Obsidian
tags: []
description: Cubox通过advanced uri插件导入到Obsidian中
author: ProudBenzene
type: practice
draft: false
editable: false
modified: 20230723231145
---

# Cubox 通过 Advanced Uri 插件导入 Obsidian

## 介绍

Cubox 是一款优秀的全平台「稍后读」软件，配合其浏览器插件和微信收藏助手，可以方便地收藏网上冲浪时令你一见钟情的文章，甚至是微信中的公众号文章、聊天记录或语音。每收藏一个网页，它就会自动生成「文章视图」和「网页快照」，不仅方便阅读，即使网站 404 了，也可以通过快照功能查看。

除此之外，它还可以作为*Newsletter*的接收端，汇聚整理你订阅的各种*Newsletter*文章。内置的其他功能如文章大纲、嵌套标签等也非常方便实用。如果你还没有使用过，可以输入我的推荐码 dgppze 领取 7 天会员，先体验一下😆

但是*Cubox*的标注功能目前仍有欠缺，只有**高亮**和**评论**这两种形式。同时，对于组建知识库来说，很多用户更加习惯 All in One 的 Ob。不过，目前 Cubox 默认的导出到 Ob 过程较为繁琐。

## 配置

那么这回，我就来分享一下如何一键从 Cubox 将文章视图 markdown 导出到 Ob。答案就是——使用「**动作**」！

提示：使用本方法，需要在 Ob 中先安装 [[obsidian-advanced-uri]] 插件🤗

![|300](https://cdn.pkmer.cn/images/image-20230226224438254.png!pkmer) ![|300](https://cdn.pkmer.cn/images/image-20230226224357338.png!pkmer)

按照图中提示，打开 Cubox 的动作设置界面，创建一个新的 URL 动作，并输入一串链接，即 **URL Scheme**。

![|300](https://cdn.pkmer.cn/images/image-20230226224931049.png!pkmer)

这串链接乍一看很复杂，但分解一下，就非常简单：

- 前边的 `obsidian` 直到 `vault=`，是声明你要导入到 obsidian 的某个库中；链接中间穿插的&符号用来连接不同的参数。Cubox 还提供了很多参数，可以从界面下面的紫色方块中选择。
- 等号后面的一串字符，其实是我的库名「*绛芸的文献库📖*」的 **URL 编码**。由于 Advanced URI 插件的要求，其中的库名、文件名等字符**必须要是经过 URL 编码的**，可以通过一个 [*网站*](https://www.urlencoder.io/) 完成。
- 以此类推，后面的 `filepath` 参数是指导入到 Ob 库中之后文章储存的相对路径和保存的文件名，这个根据自己的情况填写即可，**路径中如果有英文字母以外的字符也需要经过 URL 编码**。
- `mode=overwrite` 指的是即使文件存在，也将 `data` 写入 `filepath`，即**重复导出操作会覆写文件**。
- `data` 参数是笔记文件的内容，你可以从下面的紫色方块中选择你想要的内容复制上去即可。同时，在这里也可以进行简单的排版。例如在 P3 中，我就在「*标注 Markdown*」和「*内容 Markdown*」之间加了一道分界线的 md 语法，来让导出的笔记中标注和原文之间区分得更明显。

原理上，这个方法就是借助*Cubox*本身和 Ob 的**URL Scheme**功能，来实现从 Cubox 导出文章到 Ob。