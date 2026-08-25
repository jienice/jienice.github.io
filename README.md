# Jienice 图像档案

这是一个由 GitHub Pages 托管的响应式个人摄影档案。

## 添加照片

1. 将 `.jpg`、`.jpeg`、`.png`、`.webp` 或 `.avif` 文件放入 `public/archive/`。
2. 提交并推送到 `main` 分支。
3. GitHub Pages 会在构建时自动扫描目录，新照片无需手工加入页面数组。

页面不维护固定图片清单。推荐使用以下文件名格式：

```text
YYYY-MM-tag[-tag...]-xxxxx.jpg
```

- `YYYY-MM` 会显示为年月。
- 年月之后、最后一段之前的内容都会识别为标签，支持多个标签；未写标签时归入“未分类”。
- 最后一段 `xxxxx` 会作为图片标题。
- 标签或标题内部需要空格时，可以使用下划线。
- 宽高由浏览器在图片加载后自动读取。

例如，`2026-08-旅行-胶片-001.jpg` 会显示时间 `2026-08`、标签 `旅行 / 胶片`、标题 `001`。

不符合新格式的旧照片会继续使用文件名作为标题、文件修改时间作为日期，并以子目录名作为兼容标签。

例如：

```text
public/archive/
├── 2026-08-旅行-胶片-001.jpg
└── 2026-08-日常-猫咪-002.jpg
```

## 发布设置

- Source：Deploy from a branch
- Branch：main
- Folder：/(root)

`index.html` 使用 GitHub Pages 内置的 Jekyll/Liquid 在构建时读取图片目录，因此不要添加 `.nojekyll`。
