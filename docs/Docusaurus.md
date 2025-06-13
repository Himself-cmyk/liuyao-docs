# Docusaurus怎么用？用的什么语言？

> Docusaurus怎么用？用的什么语言？

Docusaurus 是一个基于 React 和 Node.js 构建的开源文档站点生成器，它主要用于创建和维护技术文档网站。这意味着当你使用 Docusaurus 时，主要会涉及到 JavaScript 或者 TypeScript（如果你选择使用 TypeScript 版本）。此外，由于 Docusaurus 支持 Markdown 和 MDX 格式的文档编写，因此你也可以使用任何文本编辑器来编写内容。

---

以下是使用 Docusaurus 的基本步骤：

### 安装

首先，你需要确保已经安装了 Node.js v16.14 或更高版本。然后，你可以通过 npm 或 yarn 来安装 Docusaurus CLI 工具，并创建一个新的项目：

```bash
npx create-docusaurus@latest my-website classic
```

或者如果你想使用 TypeScript 模板，可以添加 `--typescript` 参数：

```bash
npx create-docusaurus@latest my-website classic --typescript
```

### 启动开发服务器

安装完成后，进入项目目录并启动开发服务器：

```bash
cd my-website
npm run start
```

这将启动一个本地服务器，默认情况下可以通过访问 `http://localhost:3000` 查看你的 Docusaurus 站点。

### 添加文档或博客文章

Docusaurus 允许你轻松地添加新的文档或博客文章。你可以在 `docs` 文件夹下创建 Markdown 文件来添加文档，在 `blog` 文件夹下创建 Markdown 文件来添加博客文章。

### 配置站点

你可以通过修改 `docusaurus.config.js` 文件来自定义站点的各种设置，比如标题、标签线、网址、基础 URL、插件和主题等。

### 构建静态文件

当你准备好部署你的网站时，可以运行以下命令来构建静态文件：

```bash
npm run build
```

这会在 `build` 目录中生成静态文件，你可以将其上传到 GitHub Pages、Netlify 或 Vercel 等静态网站托管服务上。

### 部署

根据所选的静态网站托管服务，有不同的部署方法。例如，对于 GitHub Pages，你可以按照特定步骤配置 `docusaurus.config.js` 并执行 `yarn deploy` 命令来自动化部署过程。

### 插件系统

Docusaurus 提供了一个强大的插件系统，允许你扩展其功能。你可以安装官方插件或社区插件，甚至可以自己开发插件来满足特定需求。

### 国际化支持

Docusaurus 还支持国际化（i18n），使你能够为不同语言的用户提供本地化的文档体验。你可以在 `docusaurus.config.js` 中配置多语言支持，并在 `i18n` 目录下管理翻译文件。

总之，Docusaurus 使用的主要编程语言是 JavaScript，但它也提供了对 TypeScript 的良好支持。它的设计使得即使没有前端开发经验的人也能快速上手，同时为有经验的开发者提供了足够的灵活性来进行深度定制。

# next

按照你的指引，命令行出现了如下输出，请你一步步介绍接下来做什么？

> PS D:\Code\npm> npx create-docusaurus@latest cc-docs classic
>
> Need to install the following packages: create-docusaurus@3.8.1 
>
> Ok to proceed? (y) y
>
>  √ Which language do you want to use? » TypeScript
>
>  [INFO] Creating new Docusaurus project... 
>
> [INFO] Installing dependencies with npm... [SUCCESS] Created cc-docs. 
>
> [INFO] Inside that directory, you can run several commands:   
>
> `npm start`    Starts the development server.   `npm run build`    Bundles your website into static files for production.   `npm run serve`    Serves the built website locally.   `npm run deploy`    Publishes the website to GitHub pages. We recommend that you begin by typing:   `cd cc-docs`

根据你的输出，说明你已经成功创建了一个基于 **Docusaurus + TypeScript** 的文档站点项目，项目名称为 `cc-docs`。现在我们来一步步介绍接下来你可以做什么。

---

## ✅ 第一步：进入项目目录

在命令行中执行以下命令，进入刚刚创建的项目文件夹：

```bash
cd cc-docs
```

---

## ✅ 第二步：启动开发服务器

运行以下命令启动本地开发服务器：

```bash
npm start
```

这会启动一个本地开发环境，默认地址是：

```
http://localhost:3000
```

打开浏览器访问这个地址，就可以看到你的 Docusaurus 站点正在运行了！

> 🧪 小提示：当你修改了网站内容（如文档、配置等），页面会自动刷新，非常适合开发调试。

---

## ✅ 第三步：了解项目结构

你可以使用代码编辑器（如 VS Code）打开整个 `cc-docs` 文件夹，查看默认生成的项目结构：

```
cc-docs/
├── blog/               # 博客文章存放位置（可选）
├── docs/               # 技术文档 Markdown 文件
├── src/
│   ├── components/     # 自定义 React 组件
│   ├── pages/          # 自定义页面（支持 React 和 MDX）
│   └── theme/          # 主题覆盖文件（自定义主题样式）
├── static/             # 静态资源（图片、字体等）
├── docusaurus.config.ts  # 核心配置文件（网站标题、菜单、插件等）
├── package.json        # npm 包管理配置
└── tsconfig.json       # TypeScript 配置文件
```

---

## ✅ 第四步：开始添加自己的内容

### 1. 修改首页或导航栏信息

你可以打开 `src/pages/index.tsx` 或者 `docusaurus.config.ts` 来修改首页内容和顶部导航栏。

例如，在 `docusaurus.config.ts` 中可以修改网站标题、描述、菜单项等。

---


下面为你介绍如何修改 `/d:/Code/npm/cc-docs/src/pages/index.tsx` 和 `/d:/Code/npm/cc-docs/docusaurus.config.ts` 文件来修改首页内容和顶部导航栏：

#### 1. 修改 `docusaurus.config.ts` 文件

该文件可以修改网站标题、描述、菜单项等信息。

#### 修改网站标题和标签线

```typescript
// ... existing code ...
const config: Config = {
  title: '新的网站标题', // 修改为你想要的标题
  tagline: '新的标签线，恐龙依然很酷', // 修改为你想要的标签线
  favicon: 'img/favicon.ico',
  // ... existing code ...
```

#### 修改导航栏菜单项

```typescript
// ... existing code ...
themeConfig: {
  // ... existing code ...
  navbar: {
    title: '新的导航栏标题', // 修改为你想要的导航栏标题
    logo: {
      alt: '新的网站 Logo 描述',
      src: 'img/new-logo.svg', // 修改为新的 Logo 路径
    },
    items: [
      {
        type: 'docSidebar',
        sidebarId: 'tutorialSidebar',
        position: 'left',
        label: '新的教程标签', // 修改为你想要的标签名称
      },
      {to: '/blog', label: '新的博客标签', position: 'left'}, // 修改为你想要的标签名称
      {
        href: 'https://github.com/your-repo', // 修改为你自己的 GitHub 仓库地址
        label: '新的 GitHub 标签', // 修改为你想要的标签名称
        position: 'right',
      },
    ],
  },
  // ... existing code ...
```

#### 2. 修改 `src/pages/index.tsx` 文件

该文件主要控制首页的布局和内容。

#### 修改首页标题和副标题

```tsx
// ... existing code ...
function HomepageHeader() {
  const {siteConfig} = useDocusaurusContext();
  return (
    <header className={clsx('hero hero--primary', styles.heroBanner)}>
      <div className="container">
        <Heading as="h1" className="hero__title">
          新的首页大标题
        </Heading>
        <p className="hero__subtitle">新的首页副标题</p>
        <div className={styles.buttons}>
          <Link
            className="button button--secondary button--lg"
            to="/docs/intro">
            新的按钮文字 - 5min ⏱️
          </Link>
        </div>
      </div>
    </header>
  );
}
// ... existing code ...
```

通过以上修改，你可以轻松调整首页内容和顶部导航栏信息。

---

### 2. 添加技术文档

将 `.md` 或 `.mdx` 文件放入 `docs/` 目录下即可，Docusaurus 会自动将其整理成文档页面，并生成侧边栏。

示例：
新建一个文件 `docs/intro.md`：

```markdown
---
slug: /
---

# 欢迎来到我的文档中心

这是我的第一个 Docusaurus 页面！
```

然后刷新本地服务页面，就会看到新的内容啦！

---

## ✅ 第五步：构建静态文件（用于部署）

当你完成了内容编写并准备部署上线时，运行以下命令打包生产环境的静态资源：

```bash
npm run build
```

构建完成后，静态文件会出现在 `build/` 文件夹中，可以直接上传到 GitHub Pages、Vercel、Netlify 等平台。

---

## ✅ 第六步：部署网站（以 GitHub Pages 为例）

如果你希望将网站部署到 GitHub Pages，可以使用以下命令：

```bash
npm run deploy
```

⚠️ 注意：使用前需要确保：

- 项目已提交到 GitHub 仓库；
- 在 `docusaurus.config.ts` 中设置好了正确的 `url` 和 `baseUrl`；
- 如果不是用 GitHub 用户页，还需要配置 `gh-pages` 分支等。

---

## ✅ 第七步：自定义与扩展

你可以通过以下方式进一步定制你的站点：

- 使用官方插件（如 Google Analytics、搜索功能 Algolia、版本控制等）
- 自定义主题颜色、布局、组件
- 支持多语言（i18n）
- 添加博客功能
- 使用 MDX 编写更复杂的文档页面

---

## ✅ 常见问题

| 问题                     | 解决方法                        |
| ------------------------ | ------------------------------- |
| 启动失败，报错找不到模块 | 运行 `npm install` 再次安装依赖 |
| 页面空白或未更新         | 清除缓存：`npm run clear`       |
| 构建后无法访问某些页面   | 检查路由配置和 slug 设置        |

---

## ✅ 推荐学习资料

- 官方文档（中文）：https://docusaurus.io/zh-CN/docs/introduction
- GitHub 仓库：https://github.com/facebook/docusaurus
- 示例项目：https://github.com/crazyaxel/docusaurus-example-ts

---

如果你有任何具体的问题，比如“如何更换主题”、“怎么添加中文语言”、“如何集成 Algolia 搜索”，欢迎继续提问，我可以一步步帮你操作 😊

