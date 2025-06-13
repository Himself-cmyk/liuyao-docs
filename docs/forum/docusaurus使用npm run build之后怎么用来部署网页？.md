> docusaurus使用npm run build之后怎么用来部署网页？

## 部署网页
使用Docusaurus构建静态网站后，可以通过以下步骤来部署你的网页：

### 1. 本地查看

当你执行`npm run build`命令之后，Docusaurus会在项目目录下生成一个`build`文件夹，里面包含了你网站的所有静态文件。

- 要在本地查看构建后的网站，你可以使用一个简单的HTTP服务器来运行这个文件夹。如果你安装了Node.js，可以使用如下命令通过全局安装的`serve`工具来启动一个本地服务器：

```bash
npx serve -s build
```

这将会在本地启动一个服务器，并提供你构建好的网站供浏览。默认情况下，它通常会在`http://localhost:5000/`或者类似的地址上可用。

### 2. 部署到GitHub Pages

将你的Docusaurus网站部署到GitHub Pages包括几个步骤：

#### 准备工作

确保你在`docusaurus.config.js`中正确设置了`url`和`baseUrl`，以及配置了`organizationName`、`projectName`和`githubHost`（如果使用的是GitHub Enterprise，则需要指定）。

#### 自动部署

Docusaurus提供了方便的命令来自动部署到GitHub Pages：

- 如果你想要部署到GitHub Pages的`gh-pages`分支，首先确保该分支已经存在，如果没有，你可以手动创建它，或者让Docusaurus帮助你创建。
  
- 然后，在你的项目根目录下运行：

```bash
npm run deploy
```

这实际上是两个步骤的组合：首先它会运行`npm run build`来生成静态文件，然后它会把这些文件推送到你的仓库的`gh-pages`分支（或自定义分支）。

#### 手动部署

如果你想手动部署，也可以这样做：

- 先运行`npm run build`生成静态文件。
- 然后，进入`build`目录，将其内容提交到你的GitHub仓库的`gh-pages`分支（或选择其他分支作为发布源）。

请记得设置GitHub Pages从正确的分支加载页面。你可以在GitHub仓库的设置页面找到这一选项。

通过这些步骤，你应该能够成功地将你的Docusaurus网站部署到GitHub Pages并进行访问。

## 参考文章
> 参考文章
关于使用Docusaurus构建和部署网站，确实存在一些参考文章可以提供详细的步骤和指导。以下是一些资源的概述：

1. **使用Docusaurus+ Git 优雅地搭建自己的文档和博客站点** - 这篇文章详细介绍了如何在CentOS 8 Stream云服务器环境中配置Node.js环境、部署Docusaurus、设置Nginx反向代理，并通过Git和GitHub管理站点内容。它还提供了从安装到上线的一系列操作指南。

2. **使用docusaurus搭建网站，并部署到github** - 该文侧重于介绍如何使用Docusaurus快速创建网站框架，如何运行本地开发服务器，以及如何将构建好的静态网站部署到GitHub Pages上。文中包括了具体的命令行指令和配置文件示例。

3. **[边写边学系列] — 超级好用的文档站建站框架Docusaurus** - 此文以一个寻找适合React社区的文档站工具的故事为引子，深入浅出地讲解了Docusaurus的特点、初始化项目的方法、目录结构解析等，并展示了如何修改核心配置文件来定制化你的网站。

这些文章不仅覆盖了Docusaurus的基本概念和特性，还提供了实际操作的例子，可以帮助你更好地理解和使用这个强大的静态网站生成器。如果你需要直接访问这些文章，可以通过搜索引擎查询它们的标题或者相关的关键词来找到原文进行更深入的学习。