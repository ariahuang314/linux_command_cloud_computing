# Assignment 9 指南

## 实验内容

部署一个静态网页博客。静态网页博客是一种不需要后端服务器和数据库支持的网站，只需要使用 HTML、CSS 和 JavaScript 等前端技术就可以实现。静态网页博客有很多优点，比如速度快、安全稳定、易于维护等。

你需要选择一个自己感兴趣或擅长的主题来制作一个静态网页博客，比如个人介绍、爱好分享、技术总结等。你需要设计至少四个页面来展示博客内容，不限于首页、关于我、文章列表、文章详情等。

## 实验要求

- 代码风格：你需要使用合理的缩进和空格来格式化代码，并且使用有意义的变量名和函数名来提高代码可读性。
- 注释规范：你需要在代码中添加必要的注释来说明代码逻辑和功能，并且使用统一的注释风格。
- 文件命名：你需要使用有意义且符合规范的文件名来组织代码文件，并且使用小写字母和下划线分隔单词。

- 作业提交：你需要在指定 issue 中给出博客链接，并附上自己对本次作业的总结或反思（可以把这部分内容放在博客页面中，给出对应链接即可）。
  - 提交地址：<https://github.com/X-lab2017/oss101/issues/119>
  - 提交的评论格式为 `<学号> <链接>` 例如：`123456789 https://xlab2017.yuque.com/staff-kbz9wp/ut3q7i/kf38uhpd6tl3otl0`
  - 总结或反思可以包括但不限于包括以下内容：
    - 往期实验报告（markdown）
    - 博客主题及其选取原因
    - 博客页面布局及其设计思路
    - 博客功能实现及其技术选择
    - 博客样式设计及其美学考量
    - 博客制作过程中遇到的问题及其解决方法
- 作业截止：本次作业将于 4 月 28 日开始，持续两周，请大家在截止日期（5 月 12 日）上课之前完成并提交作业。

## 基础知识

- SSG 框架
  - 一种常用的框架是 Jekyll ，它是一个 Ruby 编写的、快速、简洁且高效的静态网站生成引擎，它使用一个模板目录作为网站布局的基础框架，支持 Markdown、Textile 等标记语言的解析，提供了模板、变量、插件等功能，最终生成一个完整的静态 Web 站点。你可以在 GitHub Pages 上直接使用 Jekyll 来搭建博客，并且选择不同的主题来美化你的博客界面。
  - 另一种常用的框架是 Hexo，它也是一个快速、简洁且高效的静态网站生成引擎，它使用 Node.js 编写，并且提供了丰富的插件和主题来扩展和定制你的博客功能和外观。你可以在本地使用 Hexo 来编写和预览你的博客内容，并且通过简单的命令就能将生成的网页上传到 GitHub Pages 上。
  - 如果你想要更多选择或灵感，你可以参考以下链接中收集或推荐了一些基于 GitHub Pages 的各类开源项目模板 ，比如程序员个性化简历、程序员酷炫博客等等。这些模板都有相应的项目地址和预览地址，你可以根据自己喜欢或需要来选择或修改。[Static Site Generators - Top Open Source SSGs | Jamstack](https://jamstack.org/generators/)
- Github Actions
  - GitHub Actions 是一种在 GitHub 上自动化、定制和执行软件开发工作流程的功能。它可以帮助你在不同的事件（例如代码提交、拉取请求或标签创建）上触发不同的任务（例如构建、测试或部署）。
  - 在部署静态网页中，GitHub Actions 可以用来构建和发布 Jekyll 站点到 GitHub Pages。Jekyll 是一种简单、博客感知的静态网站生成器，它可以将 Markdown 或 AsciiDoc 等格式的文本转换为 HTML 页面，并提供各种主题和插件。
  - 使用 GitHub Actions 部署 Jekyll 站点有以下优点：
    - 控制 gemset 和 Jekyll 版本 — 你可以使用任何你想要的 Jekyll 版本，而不是受限于 GitHub Pages 默认支持的版本（目前是 3.9.0）。
    - 使用任意插件 — 你可以使用任何 Jekyll 插件，无论它们是否在 GitHub Pages 的白名单中，甚至是直接放在 `_plugins` 目录下的 `*.rb` 文件。
    - 自定义工作流管理 — 通过创建一个工作流文件来运行 Actions，你可以指定自定义的构建步骤，使用环境变量等。
- Git
  - 分布式版本控制系统，用于管理你的代码和文件。你需要使用 Git 将你的静态网页上传到 GitHub 上，同步到 GitHub Pages。
- Frontmatter
  - Frontmatter 是一种在 Markdown 文件中添加元数据的方法，它由三条虚线包围的有效的 YAML、JSON 或 TOML 格式的内容组成。
  - 在静态博客中，Frontmatter 可以用来指定一些页面的配置选项，例如标题、描述、布局、语言、标签、分类等。这些选项可以影响页面的生成和展示方式，也可以被其他组件或插件访问和使用。
- Markdown
  - Markdown 语法的官方规范可以在 [ruanyf/document-style-guide: 中文技术文档的写作规范 (github.com)](https://github.com/ruanyf/document-style-guide) 查看，其中包含了基本语法和扩展语法的说明和示例。
  - 检查 Markdown 的源代码是否规范排版正确，有以下几种方法：
    - 使用在线工具，如 Markdownlint，可以直接在网页上输入或粘贴 Markdown 源代码，然后查看是否有错误或警告提示，并按照建议进行修改。
    - 使用 VSCode 插件，如 Markdown All in One 和 Markdownlin，可以在 VSCode 编辑器中实时检查和预览 Markdown 源代码，并提供一键修复的功能。

## 实验步骤

1. 选择一个你喜欢的博客（最好从主题样式开始选择）推荐在 Jekyll 和 Hexo 之间选取。
2. 注册 github 并使用 github 的代码仓库以及 pages 功能。
3. 选取对应框架的教程文档，跟随教程完成部署并且填充内容。

PS：如果在本次实验之前已经有了自己的静态博客，可以用自己已有的提交，并且助教会请同学们分享。
