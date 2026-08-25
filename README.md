# Jienice 图像档案

这是一个由 GitHub Pages 托管的响应式个人摄影档案。

## 添加照片

1. 将 `.jpg`、`.jpeg`、`.png`、`.webp` 或 `.avif` 文件放入 `public/archive/`。
2. 提交并推送到 `main` 分支。
3. GitHub Pages 会在构建时自动扫描目录，新照片无需手工加入页面数组。

页面不维护固定图片清单：标题来自文件名，日期来自文件修改时间，宽高由浏览器读取。直接放在 `public/archive/` 的照片归入“未分类”；放入子目录时，子目录名会自动成为筛选分类。

例如：

```text
public/archive/
├── 远行/
│   └── 高原驮队.jpg
└── 日常/
    └── 花野.jpg
```

## 发布设置

- Source：Deploy from a branch
- Branch：main
- Folder：/(root)

`index.html` 使用 GitHub Pages 内置的 Jekyll/Liquid 在构建时读取图片目录，因此不要添加 `.nojekyll`。
