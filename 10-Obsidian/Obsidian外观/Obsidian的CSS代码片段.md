---
uid: 20230329145845
title: Obsidian 的 CSS 代码片段
tags: [Obsidian, CSS, snippets, 外观, 主题]
description: Obsidian 的 CSS 代码片段
author: OS
type: awesome
draft: false
editable: false
modified: 20230718232910
aliases: [Obsidian css代码片段]
---

# Obsidian 的 CSS 代码片段

主题可以帮助你获得更加的视觉和交互体验，除了通过 设置 > 外观 > 主题，中安装的主题外。

Obsidian 还支持一种外部样式代码引用的方式。

## 位置

打开笔记仓库的 `.obsidian` 文件夹，其中如果没有 `snippets` 文件夹则创建。

在 Obsidian 中的 CSS snippets 都是以.css 的档案格式储存在特定的文件夹。如果你有将 CSS snippets 放到该文件夹，就会在 Obsidian 显示开关。

![Pasted image 20230126215854](https://cdn.pkmer.cn/images/2082fd7f6036cd4da2572868af81b729_MD5.png!pkmer)

## 使用

1、别人给你的，或者你看到不错的代码片段（CSS）文件，放进 `snippets` 文件夹就行。或者自己建立一个 CSS 文件，书写你自己的样式当然需要一点 CSS 代码基础。

2、 Obsidian > 设置 > 外观，最后一项【CSS 代码片段】，刷新一下，会显示出新增的文件，把后面的切换按钮打开即可。

涉及软件界面的修改，有时候可能需要重启软件生效。

### CSS 修改优秀范例

#### ICON

- [[回归原始的Obsidian图标]]
- [[Obsidian样式-自定义待办图标]]

#### 编辑器

- [[Obsidian样式-编辑模式下当前行高亮]]
- [[Obsidian样式-加粗粗体样式优化]]
- [[Obsidian美化代码域对编程语言的样式展示]]
- [[Obsidian样式-Callout样式]]
- [[自定义选中文本部分高亮颜色]]
- [[使用CSS-HTML实现分栏]]
- [[Obsidian样式-笔记页内标题居中]]
- [[Obsidian样式-分割线样式美化]]
- [[Obsidian样式-给笔记添加随机背景图]]
- [[Obsidian样式-段落首行增加缩进]]
- [[Obsidian样式-美化高亮样式]]
- [[Obsidian样式-美化行内代码样式]]
- [[Obsidian样式-引用框样式]]
- [[Obsidian样式-编辑模式代码块显示行号]]

#### 链接

- [[Obsidian网址前自动加图标]]
- [[Obsidian样式-修改内链的链接颜色]]

#### 文件管理器

- [[Obsidian样式-文件浏览器样式]]
- [[Obsidian样式-文件管理名称滚动效果]]
- [[Obsidain美化-自定义文件夹图标]]

#### 段落

- [[Obsidian样式-如何自定义段落前后间距]]
- [[Obsidian样式-特殊标签-让Markdown的文本多彩多色]]

#### 列表、待办

- [[Obsidian样式-待办完成样式]]
- [[Obsidian样式-自定义待办图标]]
- [[Obsidian样式-待办事项美化复选框]]
- [[Obsidian样式-自定义大纲缩进线样式]]

#### 引用

- [[Obsidian样式-隐藏块引用ID]]

#### 表格样式

- [[Obsidian样式-表格样式简明方法]]

#### 标签样式

- [[Obsidian样式-多彩tag样式]]

### 标签页

- [[Obsidian样式-标签页Tab样式]]

#### 白板（Canvas）

- [[Obsidian样式-canvas白板卡片中文字居中]]
- [[Obsidian样式-Canvas样式的修改及增强卡片的显示效果]]

#### dataview

- [[Obsidian样式-建立书籍电影的卡片化视图]]

#### 移动端

[[通过css在移动端右下角添加源码和阅读转换按钮]]

#### 插件样式

- [[Obsidian-calendar插件的样式修改]]
- [[DataView在table视图下标签出现错位断裂的修复]]

## 自定义 CSS 简单上手指南

如果你正在设计你个性化的 CSS，你可以通过使用开发者工具来获得更多元素信息，提高设计效率。使用开发者工具

- 在 Windows 或 Linux 下，使用快捷键 `Ctrl+Shift+I`；
- 在 macOS 下，使用快捷键 `Cmd+Opt+I` 即可。

按下后会出现类似下图的样式。不用被这些代码吓住，这其实就是当前页面的 css 代码。

![image.png](https://cdn.pkmer.cn/images/202305042054692.png!pkmer)

比如这里你想修改标题颜色只需要点击这个箭头

![image.png](https://cdn.pkmer.cn/images/202305042055323.png!pkmer)

然后把鼠标指向要修改的元素，这里指向标题

![image.png](https://cdn.pkmer.cn/images/202305042057355.png!pkmer)

这里的 `span.cm-header.cm-header-1` 就是标题对应的 css 选择器。

同时左侧调试窗口的内容也变成了 标题对应的 css 设置。

![image.png](https://cdn.pkmer.cn/images/202305042100564.png!pkmer)

在这里我们发现一条规则 `.HyperMD-header-1, .inline-title[data-level='1'], .HyperMD-list-line .cm-header-1` 里面包含了 .cm-header-1 就是我们要修改的选择器。

```css
.HyperMD-header-1, .inline-title[data-level='1'], .HyperMD-list-line .cm-header-1 {
    font-variant: var(--h1-variant);
    letter-spacing: -0.015em;
    line-height: var(--h1-line-height);
    font-size: var(--h1-size);
    color: var(--h1-color);
    font-weight: var(--h1-weight);
    font-style: var(--h1-style);
    font-family: var(--h1-font);
}
```

通过字母含义不难看出 color 就是负责颜色的。 这里的值为 `var(--h1-color)` 其实用了 css 的高级写法，我们先不用管它怎么写，双击 `var(--h1-color)` 这个值，删除后浏览器预设一些颜色值，可供选择，这里的颜色可以输入名称，也支持十六进制色值。

![image.png](https://cdn.pkmer.cn/images/202305042108839.png!pkmer)

设置好颜色后，会立马在 Obsidian 看到修改后的效果，但这个只是临时效果，重启后就消失了，要永久生效，需要把规则保存为 css 代码片段。

对这条 css 右键 - 复制规则，即可把 css 片段内容复制到剪贴板中。

![image.png](https://cdn.pkmer.cn/images/202305042111606.png!pkmer)

`

新建一个 css 文件 比如 my.css 把复制的内容粘贴进去，保存即可。

然后参考这里 [[Obsidian的CSS代码片段|Obsidian css代码片段]] 启用 my.css 片段 就可以看到效果了。

## 延伸阅读

修改样式目前有下面几种途径

- 使用社区主题，根据主题带的设置项调整
- 根据上面教程 自己找到 css 选择器，自己写 css 片段
- 找到别人分享的 css 片段的内容，复制到自己的片段中
- 通过 style setting 插件修改，建议安装 [[obsidian-style-settings]] 并使用默认主题片段 ![[obsidian-style-settings#^992e4d]]
