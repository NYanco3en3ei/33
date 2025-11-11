# 销售订单管理系统

这是一个基于React和TypeScript的销售订单管理系统，支持管理员和业务员两种角色，提供产品管理、订单管理、客户管理和数据统计功能。

## 功能特点

- 👤 角色权限管理（管理员/业务员）
- 📦 产品管理（添加、编辑、删除产品）
- 📋 订单管理（创建、查看、更新订单状态）
- 👥 客户管理（添加、编辑、删除客户信息）
- 📊 数据统计仪表板（销售趋势、订单状态分布）
- 🌓 深色/浅色主题切换
- 📱 响应式设计，支持移动端和桌面端

## 技术栈

- **前端框架**: React 18+
- **编程语言**: TypeScript
- **构建工具**: Vite
- **样式框架**: Tailwind CSS
- **路由管理**: React Router
- **状态管理**: Context API + Local Storage
- **UI组件**: Font Awesome, Framer Motion
- **数据可视化**: Recharts

## 快速开始

### 前提条件

确保您的系统已安装以下软件：

- Node.js (v16+)
- pnpm (推荐的包管理器)

### 安装依赖

1. 克隆仓库到本地
```bash
git clone <your-github-repo-url>
cd sales-order-management-system
```

2. 安装项目依赖
```bash
pnpm install
```

### 开发模式

启动开发服务器：
```bash
pnpm dev
```

应用将在 http://localhost:3000 启动。

### 构建生产版本

构建用于部署的生产版本：
```bash
pnpm build
```

构建后的文件将生成在 `dist` 目录中。

## 部署指南

### 选项 1: Vercel 部署

1. 访问 [Vercel](https://vercel.com/) 并登录您的账户
2. 点击 "New Project"
3. 选择您的 GitHub 仓库
4. 保持默认配置，点击 "Deploy"
5. 等待部署完成，获取生成的URL

### 选项 2: Netlify 部署

1. 访问 [Netlify](https://www.netlify.com/) 并登录您的账户
2. 点击 "Add new site" > "Import an existing project"
3. 选择您的 GitHub 仓库
4. 在构建配置中设置:
   - Build command: `pnpm build`
   - Publish directory: `dist`
5. 点击 "Deploy site"

### 选项 3: GitHub Pages 部署

1. 安装 `gh-pages` 包:
```bash
pnpm add -D gh-pages
```

2. 在 `package.json` 中添加脚本:
```json
"scripts": {
  "deploy": "gh-pages -d dist"
}
```

3. 构建并部署:
```bash
pnpm build
pnpm deploy
```

### 选项 4: 自定义服务器部署

1. 构建项目:
```bash
pnpm build
```

2. 将 `dist` 目录中的文件部署到您的Web服务器的根目录

## 数据存储说明

本项目使用浏览器的 Local Storage 进行数据存储，所有数据仅保存在用户的本地浏览器中。这意味着：

- 不同用户之间的数据不共享
- 清除浏览器缓存可能会导致数据丢失
- 如需要持久化存储和多用户共享，请考虑集成后端API

## 登录信息

系统预设了以下账户：

- **管理员账户**:
  - 用户名: admin
  - 密码: password

- **业务员账户**:
  - 用户名: sales1 或 sales2
  - 密码: password

## 角色权限说明

- **管理员**: 可以访问所有功能，包括产品管理、订单管理、客户管理和数据统计
- **业务员**: 可以创建和查看订单、查看产品信息，但不能修改或删除产品和客户

## 后续操作建议

1. **个性化定制**:
   - 修改 `index.html` 中的标题和元信息
   - 自定义颜色主题（修改相关组件中的Tailwind类）

2. **功能扩展**:
   - 添加产品分类功能
   - 实现订单搜索和筛选
   - 添加更详细的数据分析报表
   - 集成后端API进行真实数据存储

3. **性能优化**:
   - 实现组件懒加载
   - 优化大型数据集的渲染
   - 添加数据导出功能（如导出为Excel）

4. **安全性增强**:
   - 实现更安全的认证机制
   - 添加数据验证和错误处理
   - 实现请求频率限制

## License

MIT