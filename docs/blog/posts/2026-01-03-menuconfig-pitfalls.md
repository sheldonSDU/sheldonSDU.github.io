---
title: ESP-IDF menuconfig 常见坑
date: 2026-01-03
cover: assets/cover-menuconfig.svg
excerpt: menuconfig 选项不显示、sdkconfig 覆盖、Kconfig 放置位置等高频问题总结。
tags: [esp-idf, kconfig, troubleshooting]
---
# ESP-IDF menuconfig 常见坑

## 1) 选项不显示
通常是 `depends on` 条件未满足。

## 2) sdkconfig 被覆盖
建议通过 `idf.py menuconfig` 修改，避免手改。

## 3) 组件 Kconfig 放置位置
- `Kconfig`：组件内
- `Kconfig.projbuild`：提升到项目层
