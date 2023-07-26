---
uid: 20230505141041
title: Obsidian 样式：文件浏览器样式
tags: [Obsidian, css, 文件浏览器, 插件, 样式]
description: Obsidian 样式：文件浏览器样式
author: cuman
type: other
draft: false
editable: false
modified: 20230703104612
---

# Obsidian 样式：文件浏览器样式

## 概述

Obsidian 自带的文件浏览器，样式单一，有很大的改造余地，通过 css 可以让文件夹变的更醒目更个性化。

## 文件夹添加图标

根据自己的文件夹名称，把名称写到 css 中就可以自定义文件夹图标，其中文件夹图标使用的是 svg 格式，[iconfont-阿里巴巴矢量图标库](https://www.iconfont.cn/) 这里有很多图标可供选择。css 中 svg 图标需要转成 base64 格式才能正确解析，通过这个网页实现转换 [SVG to CSS converter | SVG Backgrounds](https://www.svgbackgrounds.com/tools/svg-to-css/)

### 效果

假设这里的文件夹名称为 `000 Inbox`，`100 Projects` 等

 ![image.png](https://cdn.pkmer.cn/images/202305051414251.png!pkmer)

### 代码

```css
/* Obsidian snippet to add icons to certain folders in the explorer view */
.nav-file-title-content, .nav-folder-title-content
{
display: flex;
}
.nav-folder .nav-folder-title[data-path="000 Inbox"] .nav-folder-title-content::before{
  margin: 0 4px 0 0;
  height: 17px;
  width: 17px;
  display: inline-block;
  content: "";
  background-size: 17px 17px;
  background-repeat: no-repeat;
  background-position-y: 1px;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='24' height='24' viewBox='0 0 24 24' fill='none' stroke='%239da9a0' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Cpolyline points='22 12 16 12 14 15 10 15 8 12 2 12'%3E%3C/polyline%3E%3Cpath d='M5.45 5.11 2 12v6a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2v-6l-3.45-6.89A2 2 0 0 0 16.76 4H7.24a2 2 0 0 0-1.79 1.11z'%3E%3C/path%3E%3C/svg%3E");
}

.nav-folder .nav-folder-title[data-path="100 Projects"] .nav-folder-title-content::before{
  margin: 0 4px 0 0;
  height: 17px;
  width: 17px;
  display: inline-block;
  content: "";
  background-size: 17px 17px;
  background-repeat: no-repeat;
  background-position-y: 1px;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='24' height='24' viewBox='0 0 24 24' fill='none' stroke='%239da9a0' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Cpath d='M8 17h12a2 2 0 0 0 2-2V9a2 2 0 0 0-2-2h-3.93a2 2 0 0 1-1.66-.9l-.82-1.2a2 2 0 0 0-1.66-.9H8a2 2 0 0 0-2 2v9c0 1.1.9 2 2 2Z'%3E%3C/path%3E%3Cpath d='M2 8v11c0 1.1.9 2 2 2h14'%3E%3C/path%3E%3C/svg%3E");
}

.nav-folder .nav-folder-title[data-path="200 Areas"] .nav-folder-title-content::before{
  margin: 0 4px 0 0;
  height: 17px;
  width: 17px;
  display: inline-block;
  content: "";
  background-size: 17px 17px;
  background-repeat: no-repeat;
  background-position-y: 1px;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='24' height='24' viewBox='0 0 24 24' fill='none' stroke='%239da9a0' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Cpath d='m3 9 9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z'%3E%3C/path%3E%3Cpolyline points='9 22 9 12 15 12 15 22'%3E%3C/polyline%3E%3C/svg%3E");
}

.nav-folder .nav-folder-title[data-path="300 Resources"] .nav-folder-title-content::before{
  margin: 0 4px 0 0;
  height: 17px;
  width: 17px;
  display: inline-block;
  content: "";
  background-size: 17px 17px;
  background-repeat: no-repeat;
  background-position-y: 1px;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='24' height='24' viewBox='0 0 24 24' fill='none' stroke='%239da9a0' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Cpolygon points='12 2 2 7 12 12 22 7 12 2'%3E%3C/polygon%3E%3Cpolyline points='2 17 12 22 22 17'%3E%3C/polyline%3E%3Cpolyline points='2 12 12 17 22 12'%3E%3C/polyline%3E%3C/svg%3E");
}

.nav-folder .nav-folder-title[data-path="400 Archives"] .nav-folder-title-content::before{
  margin: 0 4px 0 0;
  height: 17px;
  width: 17px;
  display: inline-block;
  content: "";
  background-size: 17px 17px;
  background-repeat: no-repeat;
  background-position-y: 1px;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='24' height='24' viewBox='0 0 24 24' fill='none' stroke='%239da9a0' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Crect x='2' y='4' width='20' height='5' rx='2'%3E%3C/rect%3E%3Cpath d='M4 9v9a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V9'%3E%3C/path%3E%3Cpath d='M10 13h4'%3E%3C/path%3E%3C/svg%3E");
}

.nav-folder .nav-folder-title[data-path="999 Templates"] .nav-folder-title-content::before{
  margin: 0 4px 0 0;
  height: 17px;
  width: 17px;
  display: inline-block;
  content: "";
  background-size: 17px 17px;
  background-repeat: no-repeat;
  background-position-y: 1px;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='24' height='24' viewBox='0 0 24 24' fill='none' stroke='%239da9a0' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Cpath d='M21 3H3v7h18V3z'%3E%3C/path%3E%3Cpath d='M21 14h-5v7h5v-7z'%3E%3C/path%3E%3Cpath d='M12 14H3v7h9v-7z'%3E%3C/path%3E%3C/svg%3E");
}

.nav-folder .nav-folder-title[data-path="Daily Notes"] .nav-folder-title-content::before{
  margin: 0 4px 0 0;
  height: 17px;
  width: 17px;
  display: inline-block;
  content: "";
  background-size: 17px 17px;
  background-repeat: no-repeat;
  background-position-y: 1px;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='24' height='24' viewBox='0 0 24 24' fill='none' stroke='%239da9a0' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Crect x='3' y='4' width='18' height='18' rx='2' ry='2'%3E%3C/rect%3E%3Cline x1='16' y1='2' x2='16' y2='6'%3E%3C/line%3E%3Cline x1='8' y1='2' x2='8' y2='6'%3E%3C/line%3E%3Cline x1='3' y1='10' x2='21' y2='10'%3E%3C/line%3E%3C/svg%3E");
}



```

## 文件添加图标

为了突出某个文件，可以对这个文件进行样式设计，比如加一个醒目的图标。

### 效果

假设有个文件名称为 `Workbench.md`

![image.png](https://cdn.pkmer.cn/images/202305051420985.png!pkmer)

### 代码

```css
.nav-file .nav-file-title[data-path="Workbench.md"] .nav-file-title-content::before{
  margin: 0 4px 0 0;
  height: 17px;
  width: 17px;
  display: inline-block;
  content: "";
  background-size: 17px 17px;
  background-repeat: no-repeat;
  background-position-y: 1px;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='24' height='24' viewBox='0 0 24 24' fill='none' stroke='%239da9a0' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Cpath d='M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z'%3E%3C/path%3E%3Cpolyline points='7.5 4.21 12 6.81 16.5 4.21'%3E%3C/polyline%3E%3Cpolyline points='7.5 19.79 7.5 14.6 3 12'%3E%3C/polyline%3E%3Cpolyline points='21 12 16.5 14.6 16.5 19.79'%3E%3C/polyline%3E%3Cpolyline points='3.27 6.96 12 12.01 20.73 6.96'%3E%3C/polyline%3E%3Cline x1='12' y1='22.08' x2='12' y2='12'%3E%3C/line%3E%3C/svg%3E");
}
```

## 突出文件类型

![54.gif](https://cdn.pkmer.cn/images/202306161340460.gif!pkmer)

```css

.nav-file .nav-file-title[data-path*=".pdf"] .nav-file-tag{
    background-color: rgb(240, 167, 182);
    color:white;
}

.nav-file .nav-file-title[data-path*=".png"] .nav-file-tag{
    background-color: rgb(100, 100, 168);
    color:white;
}

.nav-file .nav-file-title[data-path*=".jpg"] .nav-file-tag{
    background-color: rgb(100, 168, 124);
    color:white;
}
.nav-file .nav-file-title[data-path*=".svg"] .nav-file-tag{
    background-color: rgb(237, 182, 131);
    color:white;
}
```

## 多彩文件夹样式

[[Obsidian样式-多彩文件夹样式]]