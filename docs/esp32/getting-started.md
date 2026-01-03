# Getting Started

## 1. 添加新页面
在 `docs/` 下创建 Markdown，例如：

```
docs/esp32/adc.md
```

然后在 `mkdocs.yml` 的 `nav` 里加入：

```yaml
nav:
  - ESP32:
      - esp32/index.md
      - esp32/adc.md
```

## 2. 插入代码块
```c
printf("Hello ESP32!\n");
```

## 3. 提示框（admonition）
!!! tip "小技巧"
    Material 主题支持很多扩展语法。
