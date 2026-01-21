---
title: 基于VsCode的Draw.io 插件绘制框图
date: 2026-01-21
cover: assets/cover-ota.svg
excerpt: 基于Visual Studio Code 的 Draw.io 插件绘制框图并导出高清图的流程。
tags: [vscode, drawio, plugin, workflow]
---

## 概述
Draw.io是开源的流程图、UML 图和各种图表绘制工具。相较于Office里的Visio,Draw.io不仅具有轻量级的特点，也能同时在Windows和Linux系统使用。

Draw.io提供了面向VSCode的插件，在VsCode中绘制框图(流程图)，可以快速地将代码逻辑、数据流等可视化呈现，提高开发效率的同时，也加快了文档的编写速度。

在大模型时代，文字撰写、编码甚至画图都可以通过大模型这个得力助手来完成，但是大模型的输出结果往往需要人工进行二次编辑和优化，而这个过程往往需要借助一些辅助工具。框图的绘制可以借助大模型生成的文本描述，然后通过VSCode中的Draw.io插件进行编辑修改，最终生成高质量的框图。

下面整理下如何安装Draw.io插件，以及如何使用它来绘制框图并导出高清图的流程。

## 1.安装Draw.io插件
打开VsCode，然后按照以下步骤安装 Draw.io 插件：

1. 点击左侧的扩展图标（或使用快捷键 `Ctrl+Shift+X`）。
2. 在搜索框中输入 `draw.io`。
3. 找到 `Draw.io Integration` 插件，点击安装。

![draw.io安装教程](../imgs/draw.io安装流程.png "Draw.io安装教程")

## 2.使用Draw.io插件绘制框图
### 2.1 从零开始创建框图
1. 在VS Code中打开一个新的文件（或已有的文件）。
2. 点击顶部菜单的 `View → Command Palette`（或使用快捷键 `Ctrl+Shift+P`）。
3. 在命令面板中输入 `Draw.io`，点击执行 New Draw.io Diagram。
![draw.io创建文件](../imgs/draw.io创建文件.png "Draw.io创建文件")

4. Draw.io 插件会在侧边栏打开一个新的 Draw.io 窗口。
5. 在 Draw.io 窗口中，使用鼠标或键盘绘制框图。可以使用 Draw.io 提供的各种工具（如矩形、椭圆、箭头等）来绘制不同的元素。
6. 绘制完成后，点击顶部菜单的 `File → Export as...`，选择导出为高清图（如 PNG、JPEG 等）。
### 2.2 从文本描述创建框图

## 3.导出高清图
1. 在 Draw.io 窗口中，点击 `File → Export as...`。
2. 在导出对话框中，选择导出为高清图的格式（如 PNG、JPEG 等）。
3. 点击 `Export` 按钮，选择保存导出的高清图文件。

这里有个小技巧：导出png格式的图片时，建议设置图像的缩放比例，以获得更好的清晰度。

![draw.io导出png](../imgs/draw.io导出png.png "Draw.io导出png")

## 注意事项

