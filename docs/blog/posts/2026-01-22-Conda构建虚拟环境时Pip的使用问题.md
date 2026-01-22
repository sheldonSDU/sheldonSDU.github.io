---
title: Conda构建虚拟环境时Pip的使用问题
date: 2026-01-22
excerpt: 从 Conda 构建虚拟环境时Pip的使用问题到解决方法的完整流程。
tags: [conda, pip, virtual environment]
---
# Conda构建虚拟环境时Pip的使用问题

## 问题描述

最近在使用mkdocs构建文档时，遇到了一个问题：在虚拟环境中安装了mkdocs相关的包后，发现无法正常使用"mkdocs serve"命令启动文档服务器。提示错误为：
```
mkdocs : 无法将“mkdocs”项识别为 cmdlet、函数、脚本文件或可运行程序的名称。请检查名称的拼写，如果包括路径，请确保路径正确，然后再试一次。
所在位置 行:1 字符: 1
+ mkdocs
+ ~~~~~~
    + CategoryInfo          : ObjectNotFound: (mkdocs:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```
经过排查，发现是因为在Conda构建虚拟环境时，Pip安装的包没有被正确识别，导致mkdocs无法找到配置文件。

## 原因分析

当使用Conda创建虚拟环境时，通常采用  ``` conda install [package]``` 的方式安装包，这种方式会优先从Conda的仓库中获取包，并将其安装到虚拟环境中。然而，有些包（如mkdocs）在Conda仓库中可能没有所需版本；这时，我们会选择使用``` Pip install [package] ```的方式安装包。当所创建的虚拟环境中没有pip时，```pip install```命令会调用我们缺省环境中的pip，从而导致包被安装到了缺省环境中，而不是当前的虚拟环境中。因此，我们反复用安装时，尽管提示相应的包已安装完成，但仍然无法使用安装后的包。

## 解决方法

为了解决上述问题，我们需要确保在Conda创建的虚拟环境中正确安装并使用Pip。
    
   ```
   创建Conda虚拟环境时，使用--name参数指定环境名称，并添加pip包：
   > conda create --name myenv  pip
   ```