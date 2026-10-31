# 摄影杂谈：发布说明

## 添加一条动态

在 `_photography/` 下新建 Markdown 文件，例如 `_photography/2026-10-31-autumn.md`：

```yaml
---
title: 秋日散步
date: 2026-10-31 16:00:00 +0800
caption: 午后在公园散步，遇见一片正好的秋色。
images:
  - src: /assets/images/photography/autumn-1.jpg
    alt: 阳光下的金色树叶
  - src: /assets/images/photography/autumn-2.jpg
    alt: 林间的小路
---
```

将照片放在 `assets/images/photography/`，并在 `images` 中填写对应路径。`title` 和 `date` 用于动态标题与排序，`caption` 是动态文字，`alt` 是图片替代文本。

## 图片展示规则

- 每条动态最多展示 12 张照片；超出的照片不会显示。
- 一张照片以较大尺寸展示；两张照片并排；三张及以上按三列网格排列。
- 点击照片可打开原图。
- 可省略 `caption`；`alt` 省略时会使用动态标题。
