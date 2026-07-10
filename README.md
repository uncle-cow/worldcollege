# 🌍 World College - 全球大学升学指南

为全球华人提供最全面的大学升学信息和指导的静态网站。支持本科、研究生、博士等多个阶段的申请信息。

## ✨ 特性

- 🎨 **毛玻璃苹果风格设计** - 使用 TailwindCSS 实现现代化、简洁的 UI
- 🗺️ **交互式地图** - 展示世界顶尖大学的地理位置分布
- 📊 **权威排名汇聚** - QS、THE、ARWU 等多家权威排名
- 📚 **完整大学数据库** - 500+ 所世界名校的详细信息
- 📖 **详细申请指南** - 本科、研究生、博士等多阶段指导
- 📰 **最新资讯动态** - 招生录取、移民政策、就业实习等信息
- 🚀 **快速部署** - 支持 GitHub Pages 自动化部署

## 🛠️ 技术栈

- **Astro** - 静态网站生成器
- **TailwindCSS** - CSS 工具库
- **Leaflet** - 地图库
- **TypeScript** - 类型安全

## 📦 快速开始

### 前置要求
- Node.js 18+
- npm 或 yarn

### 安装依赖

```bash
npm install
```

### 本地开发

```bash
npm run dev
```

访问 `http://localhost:4321` 查看网站。

### 构建

```bash
npm run build
```

构建文件将输出到 `dist/` 目录。

### 本地预览

```bash
npm run preview
```

## 🚀 部署到 GitHub Pages

### 1. 配置 GitHub 仓库

首先需要修改 `astro.config.mjs` 中的部署信息：

```javascript
export default defineConfig({
  site: 'https://yourusername.github.io',
  base: '/worldcollege', // 如果部署在子路径
})
```

### 2. 上传到 GitHub

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/yourusername/worldcollege.git
git branch -M main
git push -u origin main
```

### 3. GitHub Pages 设置

1. 访问仓库 Settings
2. 在 "Pages" 部分选择部署源为 "GitHub Actions"
3. 等待自动部署完成

部署后可以在 `https://yourusername.github.io/worldcollege` 访问网站。

## 📁 项目结构

```
worldcollege/
├── .github/
│   └── workflows/
│       └── deploy.yml          # GitHub Actions 部署配置
├── src/
│   ├── layouts/
│   │   └── Layout.astro        # 主布局
│   ├── pages/
│   │   ├── index.astro         # 首页
│   │   ├── rankings.astro      # 排名页面
│   │   ├── universities.astro  # 大学数据库
│   │   ├── guides.astro        # 申请指南
│   │   └── news.astro          # 最新资讯
│   ├── styles/
│   │   └── global.css          # 全局样式
│   └── components/             # 可重用组件
├── public/
│   ├── favicon.svg
│   └── favicon.ico
├── astro.config.mjs            # Astro 配置
├── tailwind.config.js          # Tailwind 配置
└── package.json
```

## 🎯 待完成功能

- [ ] 从互联网爬取和更新大学排名数据
- [ ] 建立完整的大学数据库（前 500 名学校）
- [ ] 实现大学搜索和筛选功能
- [ ] 添加大学详情页面
- [ ] 收集和展示申请指南内容
- [ ] 实现资讯订阅功能
- [ ] 添加国际生录取数据可视化
- [ ] 实现多语言支持（英文、中文简体、中文繁体）

## 📝 内容管理

网站支持 Markdown 格式的内容：

- 在 `src/pages/` 中创建 `.md` 文件作为新页面
- 在内容中使用 Markdown 语法
- Astro 会自动将其转换为 HTML

## 🤝 贡献

欢迎提交 Pull Request 或 Issue！

## 📄 许可证

MIT License

## 📞 联系方式

如有问题或建议，请通过以下方式联系：
- GitHub Issues
- Email: contact@worldcollege.edu
