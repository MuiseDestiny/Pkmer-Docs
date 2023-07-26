---
uid: 20230504185734
title: Obsidian 插件：Quick Explorer 为标题增加面包屑导航功能
tags: [Obsidian, 插件, 面包屑导航]
description: Obsidian 插件：Quick Explorer 为标题增加面包屑导航功能
author: OS
type: other
draft: false
editable: false
modified: 20230604174658
---

# Obsidian 插件：Quick Explorer 为标题增加面包屑导航功能

## 概述

Obsidian 原有的标题栏导航条只能提供两种简单的功能，快速修改文件标题 和 定位所选目录的在文件管理器中的位置。

但面对我们日益增长的笔记，长目录管理和切换会成为一个痛点。Quick Explorer 很好的模拟了我们常见的面包屑导航功能，提供了笔记和目录快速切换的能力。

> [!Note] 插件名片
> - 插件名称：Quick Explorer
> - 插件作者：PJ Eby
> - 插件说明：在应用标题栏和笔记标题栏增加面包屑导航功能，提供了笔记和目录快速切换的能力
> - 插件项目地址：[点我跳转](https://github.com/pjeby/quick-explorer)

## 效果&特性

![quick-explorer.png](https://cdn.pkmer.cn/images/quick-explorer.png!pkmer)

增加一个面包屑导航，可以每层文件夹或者笔记中进行平层的快速切换，也可以快速跳到具体某个层级中的笔记。

## 使用

- 应用标题栏：
	- 在应用程序的标题栏上增加一个面包屑导航，鼠标点击对应文件夹，或者笔记，会显示同级的文件夹和笔记。
	- 显示的同级文件夹和笔记目录，文件夹和笔记分开显示，菜单上部优先显示文件夹。
- 笔记标题栏：
	- 在笔记的标题栏增加一个面包屑导航，鼠标点击对应文件夹，或者笔记，会显示同级的文件夹和笔记。
	- 点击笔记名称， 依然是快速修改文件名
	- 点击文件夹，显示的同级文件夹目录。
	- 显示的同级文件夹和笔记目录，文件夹和笔记分开显示，菜单上部优先显示文件夹。
- 文件夹：
	- 弹出的目录菜单中，如果遇到文件夹，点击后会继续弹出下级目录结构。
	- 如果你同层级的目录或者笔记过多，过长的目录会根据鼠标滑动的位置，跟随滑动以便浏览未显示的目录结构。
	- 文件夹会在右侧显示对应包含的笔记数量
- 笔记：
	- 鼠标指向笔记的时候，会在目录结构旁边，显示一个悬浮窗口，用于快速浏览笔记内容，方便确认是否是需要跳转到的位置。
- 拖拽：
	- 你可以通过从面包屑中拖拽文件夹或者笔记，放到对应位置，以打到移动的目的，但是并不支持你拖拽文件到面包屑到导航中。

>[!Tip] 提示
>该插件没有设置选项

### 快捷键

**Browse vault**，打开包含仓库根文件夹的下拉目录结构

**Browse current folder**，打开包含活动文件所在文件夹的下拉目录结构

**Go to next file in folder**，打开当前笔记的文件夹中的下一个文件

**Go to previous file in folder**，打开当前笔记的文件夹中的上一个文件

**Go to first file in folder**，打开当前文件的文件夹中的第一个文件

**Go to last file in folder**，打开当前文件的文件夹中的最后一个文件

### 样式设置

插件 0.2.0 版本以后：如果你使用的是 0.16.3 以后的版本，想在应用的标题栏，隐藏面包屑或者仓库的版本和名称信息，则可以使用 [[obsidian-style-settings]] 插件将其关闭。

## 兼容性

- 与 Obsidian 本身
	- 当 Quick Explorer 处于激活状态时，它可能会重新格式化标题栏，以便标准的 Obsidian 应用仓库名和版本号信息出现在右侧，而不是中心，为 Quick Explorer 本身腾出空间。
- 与主题
	- Quick Explorer 使用了 Obsidian 用于突出显示高亮按钮的颜色（你可以理解成外观里面的主题色），这样在大多数主题的浅色和暗色模式下提供足够的对比度，但在某些主题中可能过于明亮或鲜艳。
	- 某些主题尝试隐藏或淡化应用的标题栏，使 Quick Explorer 的 UI 不可见。

>[!Tip] 关联推荐
> - [[novel-word-count]]：在 Obsidian 的文件资源管理器窗格中显示每个文件、文件夹和保险库的字数，以及更多其他信息。
> - [[obsidian-collapse-all-plugin]]：单击对应图标或者使用命令，展开或关闭文件管理器中的文件夹
> - [[pane-relief]]：每个窗格的历史记录、用于窗格移动和导航的快捷键等
> - [[recent-files-obsidian]]：显示最近打开的文件列表
> - [[obsidian-gallery]]：让你的笔记变成画廊
> - [[obsidian-tagfolder]]：通过笔记中的标签，重新组织所有的笔记
> - [[chronology]]：按照月历模式导航，轻松了解编辑修改锅的笔记内容。
> - [[hidden-folder-obsidian]]：在文件管理器中快速隐藏文件夹
> - [[obsidian-show-file-path]]：显示正在编辑的文件所在的路径
> - [[hidden-folder-obsidian]]：快速隐藏文件夹