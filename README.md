# 常用网址导航

一个轻量的个人网址导航首页，把日常高频网站按分类整理成卡片，支持一键直达、聚合搜索与实时筛选。单文件、零依赖，打开即用。

## 功能特性

- **10 大分类、72 个常用站点**：搜索引擎、视频网站、工具网站、AI 网站、购物网站、社交社区、学习知识、新闻资讯、音乐娱乐、生活服务
- **顶部聚合搜索**：内置百度 / 谷歌 / Bing / 必应 / 知乎五种引擎，回车即搜，并记住上次选择
- **实时时钟与问候**：按时间段显示问候语、日期与时间
- **站点实时筛选**：输入关键词即时过滤（按名称 / 描述 / 分类匹配），按 `/` 快捷键快速聚焦筛选框
- **分类快速导航**：顶部粘性分类标签，一键平滑跳转
- **响应式适配**：桌面、平板、手机均正常显示
- **零依赖**：原生 HTML / CSS / JavaScript，无构建步骤，无外部框架

## 快速开始

直接把 `index.html` 拖入浏览器即可使用；也可以部署到 GitHub Pages 或任意静态托管平台。

```bash
git clone https://github.com/Fengxiayi/myWebsite.git
cd myWebsite
open index.html   # Windows 使用 start index.html
```

**部署到 GitHub Pages（可选）**：仓库 `Settings → Pages` 中，Source 选择 `main` 分支，即可通过 `https://fengxiayi.github.io/myWebsite/` 访问。

## 目录结构

```
myWebsite/
├── index.html   # 导航首页（站点数据内置其中）
└── README.md    # 项目说明
```

## 自定义站点

所有站点数据集中在 `index.html` 的 `CATS` 数组中，每个分类是一个对象：

```js
{
  id: "search",       // 分类标识
  name: "搜索引擎",   // 分类名称
  color: "#2563EB",   // 分类主题色
  icon: "search",     // 分类图标（内联 SVG）
  sites: [
    { n: "百度", u: "https://www.baidu.com", d: "中文搜索首选" }
  ]
}
```

字段说明：

| 字段 | 含义 |
| --- | --- |
| `n` | 站点名称（卡片首字字标显示其首字符） |
| `u` | 站点链接 |
| `d` | 一句话简介 |

增删或修改站点后保存并刷新页面即可生效。

## 技术栈

- 原生 HTML + CSS + JavaScript（ES5 语法），无构建工具
- 字体通过自托管镜像加载（Noto Serif SC / Noto Sans SC），不依赖 Google Fonts
- 图标全部使用内联 SVG，无外部图片资源

## 许可

本项目仅用于个人学习与日常使用。
