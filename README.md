# Xuanyi Zhou — academic homepage

基于 al-folio v1.2 的官方核心主题（al_folio_core 1.0.15），使用 Jekyll 和 jekyll-scholar。首页和论文卡片采用本站排版，精选论文查询和内页布局沿用官方主题。

## 本地预览

使用 Ruby 3.3 和 Bundler，在项目目录运行：

```sh
bundle install
bundle exec jekyll serve
```

浏览器打开 http://localhost:4000 。运行 `bundle exec jekyll build` 生成静态目录 `dist/`。

## 更新内容

- 简介改 `_pages/about.md`。联系方式改 `_data/profile.yml`；填入自己的邮箱、Scholar 主页或正式 CV 的 PDF 文件路径，对应入口会出现。
- 发文章只需添加 `_posts/YYYY-MM-DD-title.md`，在开头填写 `title` 和 `description`。文章路径为 `/writing/title/`。
- 论文只维护 `_bibliography/papers.bib` 一处。`selected={true}` 使论文出现在首页精选列表。完整论文列表按年份和月份倒序排列。图片放在 `assets/img/`，在条目中填写 `preview`。共同一作可用 `cofirst={3}` 标记署名顺序最前的三位作者，人数按论文填写。可选字段包括 `summary`、`website`、`code`。
- 调整首页栏目顺序，编辑 `_data/sections.yml`。
- 新增简单栏目只需新建一个 Markdown 文件。例如，新建 `_sections/talks.md`：

```markdown
---
title: Talks
order: 10
---
- [演讲标题](https://example.org/talk) · 活动名、日期
```

新栏目会按 `order` 排在首页现有栏目下方。新增独立导航页时可参考 `_pages/publications.md` 的 `nav`、`nav_order`、`permalink`。

## 内容来源

首页头像由 Xuanyi Zhou 提供。论文元数据来自 arXiv，SVG-EAR 缩略图来自[项目官方 Teaser](https://svg-project.github.io/v3/assets/images/Teaser.png)，其余缩略图来自[合作者的精选论文列表](https://github.com/joyemang33/joyemang33.github.io/tree/master/assets/img/featured-publications)。CV 链接直接打开 PDF。
