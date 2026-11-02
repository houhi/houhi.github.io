# Pengfei Zhang's academic homepage

Personal academic website: https://houhi.github.io

Adapted from [luost26/academic-homepage](https://github.com/luost26/academic-homepage), under the MIT license. The site retains the template's profile sidebar, content cards, and responsive layout. Bootstrap 4.6.2 is served locally under its MIT license; no CDN assets are required.

## 更新内容

- 基本信息、简介、教育、实习、导师链接和奖项：`_data/profile.yml`
- 已发表论文：`_publications/` 中的 Markdown 文件
- 投稿中的工作保留在 `_data/manuscripts.yml`，按用户要求不在网站或 CV 展示。
- 新闻：`_news/` 中的 Markdown 文件
- 照片：`assets/images/profile.jpg`
- 导航：`_data/navigation.yml`
- 样式：`assets/css/global.css`

每次提交到默认分支后，GitHub Pages 会自动构建。主站使用仓库根目录，`baseurl` 保持为空。

CV 页面与主页共用结构化信息，在 CV 页面点 **Print / Save PDF** 可以打印或保存 PDF。

## 本地预览

推荐使用 Ruby 3.4 和 Bundler 2.6；本项目已在 Ruby 3.4.5、GitHub Pages 232 / Jekyll 3.10.0 下完成真实构建验证。安装后：

```sh
bundle install
bundle exec jekyll build
bundle exec jekyll serve
```

访问终端显示的本地地址。修改 `_config.yml` 后需要重启预览服务。

论文作者的公开展示顺序可使用 `display_authors` 单独设置；`authors` 和 BibTeX 保留出版元数据。RAMR 按作者本人说明标注共同第一作者，并将 Pengfei Zhang 放在展示列表首位。

机构 logo 来自各机构官网，论文框架图来自作者提供的原始图或论文原文，均保留原机构和作者权利。
