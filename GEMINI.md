# 项目概述

这是一个 Jekyll 项目，一个用 Ruby 编写的静态网站生成器。它使用 `minima` 主题和 `jekyll-feed` 插件。该项目配置用于生成个人博客或网站。

# 构建与运行

要在本地构建和运行此项目，您需要安装 Ruby 和 Bundler。

1.  **安装依赖：**
    ```bash
    bundle install
    ```

2.  **运行开发服务器：**
    ```bash
    bundle exec jekyll serve
    ```
    这将在 `http://localhost:4000` 启动一个本地 Web 服务器。当您更改源文件时，网站将自动重新生成。

# 开发约定

*   **内容：** 内容是用 Markdown 编写的。博客文章位于 `_posts` 目录中，并且必须遵循 `YYYY-MM-DD-标题.markdown` 的命名约定。
*   **配置：** 主要配置文件是 `_config.yml`。
*   **依赖：** Ruby gems 使用 `Gemfile` 和 Bundler 进行管理。