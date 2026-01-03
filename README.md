# my-vue-app

This is a Vue.js application generated with create-vue, featuring Vue 3, Vite, and Vue Router.

## Features

- Vue 3
- Vite
- Vue Router
- Pinia
- Element Plus (UI framework)
- ESLint
- TMDb API integration for movie posters

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```

### Lint with [ESLint](https://eslint.org/)

```sh
npm run lint
```

## TMDb API Integration

This project integrates with The Movie Database (TMDb) API to fetch movie posters and information. The API key is already configured in the application.

To use TMDb API for movie posters:
1. The API key is stored in `src/utils/tmdbApi.js`
2. Movie posters will be fetched automatically when displaying movies
3. If TMDb API is unavailable, the application will fall back to alternative image sources

For more information about TMDb API, visit: https://www.themoviedb.org/

# 电影评论网站

这是一个基于Vue3框架开发的电影评论网站，满足课程设计的所有要求。

## 技术栈

- **Vue 3**: 使用 Composition API 构建组件
- **Vue Router 4**: 处理页面路由
- **Pinia**: 状态管理
- **Element Plus**: UI 框架
- **Axios**: 数据请求（虽然项目使用模拟数据，但结构已准备好用于真实API）
- **Vite**: 构建工具

## 功能模块

1. **首页** - 包含轮播图展示热门电影
2. **电影列表页** - 展示所有电影
3. **电影详情页** - 显示电影详细信息和评论模块
4. **评论模块** - 登录用户可发布和查看评论
5. **登录注册页** - 用户认证功能

## 项目结构

```
src/
├── assets/           # 静态资源
├── components/       # 可复用组件
├── views/            # 页面组件
├── router/           # 路由配置
├── stores/           # Pinia 状态管理
├── utils/            # 工具函数
├── styles/           # 全局样式
├── App.vue           # 根组件
└── main.js           # 应用入口
```

## 安装和运行

1. 确保已安装 Node.js (版本 >= v22)
2. 安装依赖：

```bash
npm install
```

3. 启动开发服务器：

```bash
npm run dev
```

4. 访问 `http://localhost:5173`

## 技术使用说明

### Vue Router
- 位于 `src/router/index.js`
- 定义了首页、电影列表、电影详情、登录和注册路由

### Pinia 状态管理
- 位于 `src/stores/index.js`
- 管理用户登录状态、电影数据和评论数据

### Element Plus UI 框架
- 在 `src/main.js` 中全局引入
- 在各个页面组件中使用Element Plus组件，如按钮、表单、轮播图等

### Axios 数据请求
- 位于 `src/utils/api.js`
- 虽然项目使用模拟数据，但已实现完整的API请求结构

## 页面说明

1. **首页** (`views/HomeView.vue`): 包含轮播图和热门电影推荐
2. **电影列表页** (`views/MovieListView.vue`): 展示电影列表，支持搜索功能
3. **电影详情页** (`views/MovieDetailView.vue`): 显示电影详细信息，包含评论模块
4. **登录页** (`views/LoginView.vue`): 用户登录功能
5. **注册页** (`views/RegisterView.vue`): 用户注册功能

## 特殊说明

- 由于无需开发后台，项目使用模拟数据实现所有功能
- 用户登录/注册状态保存在localStorage中
- 评论功能仅对登录用户开放
- 项目符合所有UI和交互要求