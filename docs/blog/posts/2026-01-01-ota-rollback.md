---
title: OTA 回滚策略（实践）
date: 2026-01-01
cover: assets/cover-ota.svg
excerpt: 双分区、引导计数与健康检查：一套可落地的 OTA 回滚策略。
tags: [ota, release, reliability]
---
# OTA 回滚策略（实践）

## 核心目标
- 升级失败可自动回滚
- 确保设备可恢复

## 建议做法
- 双分区
- 引导计数
- 健康检查通过后才标记成功
