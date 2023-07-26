---
uid: 20230513222802
title: Obsidian 插件：Frontmatter Alias Display 让你的笔记名下直接看到别名
tags: [Obsidian, 插件, 别名显示, YAML 区域, 笔记别名]
description: Obsidian 插件：Frontmatter Alias Display 让你在文件名下直接看到别名
author: Bon
type: other
draft: false
editable: false
modified: 20230531200129
---

# Obsidian 插件：Frontmatter Alias Display 让你的笔记名下直接看到别名

## 概述

如果你喜欢用卢曼的方式来制作笔记，那你可能会遇到一个困难，例如如果你用数字 + 字母的形式来命名题目，那你总会碰到一大堆让你徒增理解困难的文件标题，尤其是当你需要在文件浏览器中寻找这个笔记的时候，那就会非常困难，而这个插件就是为了解决这个问题而存在的。

> [!Note] 插件名片
> - 插件名称：Frontmatter Alias Display
> - 插件作者：muhammadv-i
> - 插件说明：让你在文件名下直接看到别名。
> - 插件项目地址：[点我跳转](https://github.com/muhammadv-i/obsidian-frontmatter-alias-display)

## 效果&特性

![image.png](https://cdn.pkmer.cn/images/20230514131806.png!pkmer)

## 使用

- 在你启用该插件后，你需要在你的文件的 YAML 区域内加上 [[Obsidian的YAML和Frontmatter]] Alias，例如下边的这种：

```yaml
---
aliases: ["这是一个笔记别名"]
---
```

然后这个笔记在文件浏览器中就会在其文件名的底部显示出**" 这是一个笔记别名 "** 。

> [!tip]
> - 该特性暂不支持 Graph View；
> - 还不支持其它的设置；

> [!Tip] 推荐阅读
> - [[obsidian-metatable]]：美化 frontmatter 的显示样式
> - [[obsidian-view-mode-by-frontmatter]]：自定义每个笔记的视图
> - [[metaedit]]：帮你快捷管理 Obsidian 的元数据，可以预设 YAML 区域的值
> - [[obsidian-meta-bind-plugin]]：让你的笔记具有交互性，通过各种控件修改笔记信息