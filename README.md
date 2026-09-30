# 仓库说明

本仓库是一个纯静态个人博客，托管在 GitHub Pages（wh1tZz5.github.io）。

## 目录结构

- `index.html` 首页（Hero + 最新文章列表）
- `about.html` 关于页
- `projects.html` 项目页
- `404.html` 404 页面（GitHub Pages 自动使用）
- `blog/` 文章列表与各篇正文（纯 HTML 维护）
- `css/style.css` 全站共享样式（设计变量、导航、卡片、页脚、响应式、动画）
- `css/article.css` 文章正文样式（排版、代码块、表格、提示框、前后导航）
- `js/main.js` 全站脚本（导航滚动边框）
- `feed.xml` RSS 订阅
- `assets/icon.png` 站点图标
- `.idea/` JetBrains IDE 配置（已加入本地 `.idea/.gitignore`，不入仓库）

## 维护约定

- 所有页面共用同一套导航/页脚模板，新增页面时复制任意一个 HTML 文件、替换标题与正文、把导航对应项加 `class="active"`。
- 新增文章：在 `blog/` 下建 `slug.html`，在 `blog/index.html` 与首页 `index.html` 的文章列表里各加一条 `<a class="post-item">`，并在 `feed.xml` 追加一个 `<item>`。
- 改样式只改 `css/style.css` 与 `css/article.css`，不要在页面里写内联样式（少数例外见 `404.html` 的居中布局）。

## 部署

直接 `git push` 到 `main` 分支即可，GitHub Pages 自动从仓库根目录发布，无需构建步骤。
