# 页面功能

## 数学公式

需要显示数学公式时，在页面的 YAML 头部添加 `math: true`，页面才会加载 MathJax：

```yaml
---
layout: default
math: true
---
```

## 分享图片

可在页面的 YAML 头部通过 `header-img` 指定分享图片路径。未指定时不会引用默认图片。
