---
title: "Afeedrss RSS 阅读器"
description: "这是一个 RSS 阅读器前端，使用 Inoreader 的 api 服务，界面简洁"
date: "2025/4/10"
repoURL: "https://github.com/ymsjl/afeedrss"
---
### 项目概述
该项目是一个基于 Next.js 和 NextAuth.js 的 RSS 阅读器应用，旨在通过 OAuth2.0 授权集成第三方服务（如 Inoreader），为用户提供个性化的 RSS 订阅和阅读体验。项目的主要功能包括用户认证、订阅管理和内容聚合。

### 技术栈分析

###### 1. 前端框架
**Next.js:**
用于构建服务端渲染（SSR）和静态生成（SSG）的 React 应用。
提供了高性能的页面加载和 SEO 优化能力。
项目中使用了 api 路由来处理 API 请求。

###### 2. 用户认证
**NextAuth.js:**
用于实现 OAuth2.0 用户认证。
项目中配置了自定义的 OAuth 提供方（Inoreader），通过 authorization、token 和 userinfo URL 实现认证流程。
支持 JWT 和 Session 回调，用于在客户端和服务端之间传递用户信息和访问令牌。

###### 3. 后端服务
**Inoreader API:**
项目通过 Inoreader 的 OAuth2.0 接口实现用户授权和数据访问。
使用了 Inoreader 的 userinfo 接口获取用户信息，并通过 scope 参数控制权限范围（如 read 和 write）。

###### 4. 环境变量
项目依赖多个环境变量来配置 OAuth 提供方和回调 URL：
INOREADER_SERVER_URL：Inoreader 的服务器地址。
CLIENT_ID 和 CLIENT_SECRET：OAuth 客户端 ID 和密钥。
NEXTAUTH_URL：NextAuth 的回调 URL。

### 特点

- ✅ 100/100 Lighthouse performance
- ✅ Responsive
- ✅ Accessible
- ✅ SEO-friendly


## 💻 Commands

All commands are run from the root of the project, from a terminal:

Replace npm with your package manager of choice. `npm`, `pnpm`, `yarn`, `bun`, etc

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |

## 🏛️ License

MIT