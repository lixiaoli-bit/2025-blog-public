# 📘 前端工程化·部署学习笔记

> 🚀 从零到上线，一份完整的前端工程化与服务器部署知识整理

---

## 📖 目录

- [🌐 Linux / Vim / 服务器 · 基础笔记](#1-linux--vim--服务器--基础笔记)
- [🚀 Git · 服务器 · 部署笔记](#2-git--服务器--部署笔记)
- [🧩 模块化 · 工程化笔记](#3-模块化--工程化笔记)
- [⚙️ 构建工具 · Vite 从零上手](#4-构建工具--vite-从零上手)
- [⚛️ React · 组件 · 开发笔记](#5-react--组件--开发笔记)
- [🚢 数据驱动 · 部署笔记](#6-数据驱动--部署笔记)

---

## 🌐 1. Linux / Vim / 服务器 · 基础笔记

> 🖥️ 从零开始的服务器运维入门指南

本笔记涵盖了：
- 📂 Linux 基础目录结构
- ✍️ Vim 编辑器的核心操作
- 🔑 云服务器 SSH 远程连接
- 🌍 Nginx Web 服务器的安装与配置

帮助你快速理解 **从本地到公网** 的部署基础流程。

🔗 [📄 阅读全文](https://zero-to-tech.pages.dev/main) &nbsp;|&nbsp; 🏷️ `#Linux` `#Vim` `#Nginx` `#服务器`

---

## 🚀 2. Git · 服务器 · 部署笔记

> 📦 一份完整的 Git 版本控制与项目部署实战记录

内容涵盖：
- 📂 Git 本地仓库初始化
- 🔗 GitHub 远程关联与 SSH 密钥配置
- 🖥️ 服务器端 Nginx 站点配置
- 🔧 权限调试与问题排查

梳理出一条 **从零到公网** 的清晰部署路径。

🔗 [📄 阅读全文](https://zero-to-tech.pages.dev/main) &nbsp;|&nbsp; 🏷️ `#Git` `#GitHub` `#SSH` `#部署`

---

## 🧩 3. 模块化 · 工程化笔记

> 📐 深入理解前端工程化的起点——JavaScript 模块化

核心内容：
- 🔄 传统 `<script>` 标签 vs ES Module
- 📤 `import/export` 解决全局污染与依赖顺序
- 📦 第三方库（anime.js）按需加载
- 🏗️ 为构建大型应用奠定基础

🔗 [📄 阅读全文](https://zero-to-tech.pages.dev/main) &nbsp;|&nbsp; 🏷️ `#ESModule` `#模块化` `#工程化` `#JavaScript`

---

## ⚙️ 4. 构建工具 · Vite 从零上手

> ⚡ 解决模块化遗留问题的工程化利器——Vite 使用指南

详细讲解：
- 🟢 Node.js 环境搭建
- 📦 项目初始化与依赖管理
- 🔧 `dev` / `build` / `preview` 三条核心命令
- 🚀 告别繁琐请求与缓存问题，拥抱现代化开发体验

🔗 [📄 阅读全文](https://zero-to-tech.pages.dev/main) &nbsp;|&nbsp; 🏷️ `#Vite` `#构建工具` `#NodeJS` `#工程化`

---
---

## ⚛️ 5. React · 组件 · 开发笔记

> 🧩 从积木到页面——React 组件化思维入门

详细讲解：
- 🧱 组件思想：按界面单元拆分，封装结构/样式/数据/行为
- 📦 安装 React 与 Vite 插件配置
- 🪪 `ResultCard` 组件完整解读（JSX、props、ref、useEffect）
- 🏗️ 组件嵌套：`TextLabPage` 如何拼装页面
- 🌳 React 项目骨架与文件职责划分
- 🚀 从 0 新建 React 项目（`npm create vite`）

帮助你理解 **React 如何重新定义前端开发方式**——HTML 退化为挂载点，真实内容由组件渲染。

🔗 [📄 阅读全文](https://zero-to-tech.pages.dev/main) &nbsp;|&nbsp; 🏷️ `#React` `#JSX` `#组件` `#Vite`

---

## 🚢 6. 数据驱动 · 部署笔记

> 📡 从组件到公网——数据驱动界面与项目部署实战

内容涵盖：
- 📊 数据驱动界面：界面跟着“值”走（props + state + 路由）
- 📂 内容与组件分离（`site.js` 集中管理文案）
- 🔗 路由（`useRoute.js`）——把页面状态写进 URL
- 🖥️ 服务器部署全流程：
  - 安装 Node.js（nvm）
  - 拉取代码 & 安装依赖
  - `npm run build` 生成 `dist/`
  - Nginx 指向构建产物
- 🔄 日常更新流程：`git push` → `git pull` → `install` → `build`

梳理出 **工程化 React 项目从开发到公网** 的完整部署路径，与手写 HTML 部署方式形成对比。

🔗 [📄 阅读全文](https://zero-to-tech.pages.dev/main) &nbsp;|&nbsp; 🏷️ `#React` `#数据驱动` `#部署` `#Nginx` `#NodeJS`

---


