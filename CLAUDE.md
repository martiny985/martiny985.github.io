# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

# 项目概述

这是一个 Jekyll 4.4.1 静态网站项目,使用 Bootstrap 和自定义主题构建。项目采用多页面布局结构,包含轮播图、服务展示等常见企业网站功能。

# 常用命令

## 开发服务器
```bash
bundle exec jekyll serve
```
- 启动本地开发服务器在 `http://localhost:4000`
- 文件修改会自动重新生成网站
- **重要**:修改 `_config.yml` 后必须重启服务器才能生效

## 依赖管理
```bash
bundle install          # 安装或更新依赖
```

## 构建
```bash
bundle exec jekyll build  # 构建生成静态文件到 _site/ 目录
```

# 架构与项目结构

## 布局系统

项目使用两个主要布局文件:

- **`_layouts/home_style.html`**: 首页布局,包含 Bootstrap 轮播图和服务展示区块
- **`_layouts/default_style.html`**: 通用页面布局,包含基本页面结构

所有布局都引用 `_includes/` 目录中的可重用组件:
- `head.html`: HTML head 标签内容
- `header.html`: 网站导航栏
- `footer.html`: 页脚
- `script.html`: JavaScript 引用

## 前端资源

- **Bootstrap**: 位于 `assets/bootstrap/`
- **自定义样式**: `assets/css/`, `assets/scss/`, `assets/less/`
- **字体图标**: Font Awesome (`assets/font-awesome/`)
- **JavaScript**:
  - jQuery 1.10.2: `js/jquery-1.10.2.min.js`
  - WOW.js 动画: `js/wow.min.js`

## 页面和内容

- **首页**: `index.html` (使用 `home_style` 布局)
- **其他页面**: `about.html`, `blog.html`, `contact.html`, `team.html`, `404.html`
- **博客文章**: `_posts/` 目录,文件名格式为 `YYYY-MM-DD-标题.markdown`

## 配置

`_config.yml` 包含:
- 网站基本信息 (title, email, description)
- 公司信息 (company_name, address, phone, email)
- 社交媒体链接
- Jekyll 构建设置 (markdown 处理器, 插件等)

修改配置后需要重启 `jekyll serve` 才能看到效果。

# 开发注意事项

- 博客文章必须放在 `_posts/` 目录,命名遵循 `YYYY-MM-DD-标题.markdown` 格式
- 图片资源放在 `assets/img/` 目录
- 生成的网站输出到 `_site/` 目录(Git 忽略)
- Jekyll 缓存存储在 `.jekyll-cache/` 目录(Git 忽略)
