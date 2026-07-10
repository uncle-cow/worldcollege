# 🚀 World College - 快速开始指南

欢迎使用 World College！这是一个为全球华人提供大学升学信息的现代化静态网站。

## ⚡ 快速开始（5分钟）

### 1. 安装依赖
```bash
npm install
```

### 2. 本地开发
```bash
npm run dev
```
然后访问 `http://localhost:4321` 查看网站。

### 3. 构建生产版本
```bash
npm run build
```
生成的文件位于 `dist/` 目录。

## 📁 文件夹结构解析

| 文件夹 | 说明 |
|--------|------|
| `src/pages/` | 网站的各个页面 |
| `src/layouts/` | 页面布局模板 |
| `src/styles/` | 全局样式和自定义样式 |
| `public/` | 静态资源（图片、字体等）|
| `dist/` | 构建输出（发布内容）|

## 📝 常见编辑任务

### 编辑首页内容
编辑文件：`src/pages/index.astro`

### 编辑导航栏
编辑文件：`src/layouts/Layout.astro` 中的 `<nav>` 部分

### 编辑全局样式
编辑文件：`src/styles/global.css`

### 添加新页面
1. 在 `src/pages/` 中创建新 `.astro` 文件
2. 导入 Layout：`import Layout from '../layouts/Layout.astro'`
3. 使用 Layout 包装内容

示例：
```astro
---
import Layout from '../layouts/Layout.astro'
---

<Layout title="新页面标题">
  <section class="py-20 px-4">
    <h1>新页面内容</h1>
  </section>
</Layout>
```

## 🎨 样式系统

### 毛玻璃卡片
```html
<div class="apple-card">
  内容
</div>
```

### 渐变文本
```html
<h1 class="gradient-text">标题</h1>
```

### 玻璃按钮
```html
<button class="glass-button">按钮</button>
```

## 🔗 内部链接
```astro
<a href="/rankings">查看排名</a>
<a href="/universities">大学数据库</a>
<a href="/guides">申请指南</a>
<a href="/news">最新资讯</a>
```

## 📊 添加数据

### 添加大学到排名表格
编辑 `src/pages/rankings.astro`，在表格中添加行：
```html
<tr class="border-b border-white/10 hover:bg-white/20 transition">
  <td class="px-6 py-4 font-semibold">大学名称</td>
  <td class="px-6 py-4">排名</td>
  ...
</tr>
```

### 添加新闻/资讯
编辑 `src/pages/news.astro`，复制并修改现有新闻卡片。

## 🗺️ 编辑地图

在 `src/pages/index.astro` 中编辑大学坐标数组：
```javascript
const universities = [
  { name: '大学名称', lat: 纬度, lng: 经度, rank: 排名 },
  // 添加更多...
]
```

## 🚀 部署到 GitHub Pages

详见 [DEPLOYMENT.md](DEPLOYMENT.md) 文件。

快速流程：
1. 修改 `astro.config.mjs` 中的 `site` URL
2. `git add .`
3. `git commit -m "Initial commit"`
4. `git remote add origin https://github.com/YOUR_USERNAME/worldcollege.git`
5. `git push -u origin main`
6. GitHub Pages 将自动部署

## 🔍 调试技巧

### 查看所有 Tailwind 类
使用浏览器开发者工具检查元素，或查看 `src/styles/global.css`

### 修改响应式断点
在 `tailwind.config.js` 中编辑 `theme.extend`

### 测试移动端
使用浏览器开发者工具的设备模拟功能

## 📚 常用 Tailwind 类

```
文本大小：text-sm, text-base, text-lg, text-xl
间距：p-4 (padding), m-4 (margin), gap-4
颜色：text-white, bg-blue-600, border-white/20
圆角：rounded-lg, rounded-2xl
阴影：shadow-lg, shadow-xl
过渡：transition, hover:shadow-xl
```

## ❓ 常见问题

### Q: 如何修改网站标题？
A: 编辑 `src/layouts/Layout.astro` 中的 `<title>` 标签。

### Q: 如何添加更多导航菜单项？
A: 编辑 `src/layouts/Layout.astro` 中的导航栏。

### Q: 样式没有生效？
A: 
- 确保使用了正确的 TailwindCSS 类名
- 运行 `npm run dev` 重新启动开发服务器
- 清空浏览器缓存

### Q: 如何使用自定义字体？
A: 在 `src/styles/global.css` 中使用 `@font-face`，或在 `tailwind.config.js` 中配置。

## 📖 更多资源

- [Astro 官方文档](https://docs.astro.build)
- [Tailwind CSS 文档](https://tailwindcss.com/docs)
- [Leaflet.js 文档](https://leafletjs.com/)

## 💡 下一步

1. ✅ 项目基础框架完成
2. 📊 下一步：添加真实的大学数据
3. 🔍 然后：集成搜索功能
4. 📱 最后：优化移动端体验

## 📞 获取帮助

- 查看项目文档：`README.md`, `PROJECT_SUMMARY.md`, `DEPLOYMENT.md`
- 提交 GitHub Issues
- 检查控制台错误（F12 打开开发者工具）

---

**祝你使用愉快！** 🎉

如果有任何问题或建议，欢迎反馈。
