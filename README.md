# RuoYi-Vue-Plus 技术文档

本文档旨在提供对 `RuoYi-Vue-Plus` 项目的技术栈、架构和模块的全面概述。

## 1. 项目简介

`RuoYi-Vue-Plus` 是一个基于 `Vue.js` 和 `Spring Boot` 的前后端分离的后台管理系统。它提供了一套完整的解决方案，包括用户管理、角色管理、菜单管理、定时任务、代码生成等功能。

## 2. 技术选型

### 2.1 前端 (`frontend`)

- **核心框架**: `Vue 3`
- **状态管理**: `Pinia`
- **UI 框架**: `Element Plus`
- **路由**: `Vue Router`
- **HTTP 客户端**: `axios`
- **图表**: `ECharts`
- **构建工具**: `Vite`

#### 2.1.1 项目目录

.\costa\frontend

### 2.2 后端 (`backend`)

- **核心框架**: `Spring Boot`
- **数据库**: `PostgreSQL`
- **ORM**: `MyBatis-Plus`
- **安全**: `Sa-Token`
- **任务调度**: `XXL-Job`
- **监控**: `Spring Boot Admin`
- **对象存储**: `MinIO` (通过 `ruoyi-oss` 模块集成)
- **代码生成**: `ruoyi-generator`

#### 2.2.1 项目目录

.\costa\backend

## 3. 项目结构

项目采用模块化开发，主要模块如下：

- `ruoyi-admin`: 项目的启动模块，负责整合各个模块。
- `ruoyi-common`: 通用模块，包含核心工具类、常量、枚举等。
- `ruoyi-framework`: 框架模块，包含 `Spring Security`、`MyBatis` 等核心配置。
- `ruoyi-system`: 系统模块，包含用户、角色、菜单等核心业务逻辑。
- `ruoyi-generator`: 代码生成模块，可以根据数据库表快速生成前后端代码。
- `ruoyi-job`: 定时任务模块，集成了 `XXL-Job`。
- `ruoyi-oss`: 对象存储模块，支持多种对象存储服务。
- `ruoyi-demo`: 示例模块，提供了一些示例代码。

## 4. 开发环境

- **语言**: `Java 8+`, `JavaScript (ES6+)`
- **构建工具**: `Maven` (后端), `Vite` (前端)
- **数据库**: `PostgreSQL`
- **IDE**: `IntelliJ IDEA` (推荐), `VS Code` (推荐)

## 5. 部署

- **后端**: 可以打包成 `jar` 包，通过 `java -jar` 命令运行。
- **前端**: 可以通过 `npm run build:prod` 命令打包成静态文件，然后通过 `Nginx` 等 `Web` 服务器部署。

---

希望这份技术文档能帮助您更好地理解和开发本项目。如果您有任何问题，请随时提出。
