# 部署指南 - World College

本文档说明如何将 World College 项目部署到 GitHub Pages。

## 前置条件

- GitHub 账户
- Git 命令行工具
- 已安装 Node.js 和 npm

## 部署步骤

### 第一步：在 GitHub 上创建仓库

1. 登录 GitHub 账户
2. 点击右上角的 "+" 按钮，选择 "New repository"
3. 仓库名称：`worldcollege`
4. 选择 "Public"
5. 点击 "Create repository"

### 第二步：更新配置文件

编辑 `astro.config.mjs` 文件，将以下部分替换为你的 GitHub 用户名和仓库信息：

```javascript
export default defineConfig({
  site: 'https://YOUR_USERNAME.github.io',  // 替换 YOUR_USERNAME
  base: '/worldcollege',  // 如果要部署到子路径，保持这个；否则移除
})
```

**注意**：如果要直接部署到 `https://YOUR_USERNAME.github.io`（不在子路径），删除 `base` 配置。

### 第三步：初始化 Git 并推送代码

在项目根目录运行以下命令：

```bash
# 初始化 Git
git init

# 添加所有文件
git add .

# 提交更改
git commit -m "Initial commit: World College website"

# 添加远程仓库
git remote add origin https://github.com/YOUR_USERNAME/worldcollege.git

# 重命名分支为 main
git branch -M main

# 推送到 GitHub
git push -u origin main
```

### 第四步：配置 GitHub Pages

1. 访问你的仓库主页
2. 点击 "Settings"（设置）
3. 在左侧菜单中选择 "Pages"
4. 在 "Source" 部分，选择 "Deploy from a branch"
5. 在 "Branch" 部分，选择 "main" 分支和 "/" (root) 目录
6. 点击 "Save"

### 第五步：启用 GitHub Actions

1. 访问仓库的 "Actions" 标签
2. 如果出现 workflow 可用，点击 "I understand my workflows, go ahead and enable them"
3. GitHub Actions 将自动构建并部署你的网站

### 验证部署

几分钟后，访问以下 URL：

- 如果使用了 `base: '/worldcollege'`：`https://YOUR_USERNAME.github.io/worldcollege`
- 如果没有使用 `base`：`https://YOUR_USERNAME.github.io`

## 日常更新

当你想要更新网站内容时，只需：

```bash
# 编辑文件...

# 提交更改
git add .
git commit -m "Update content"

# 推送到 GitHub
git push
```

GitHub Actions 将自动构建并部署新版本。

## 常见问题

### Q: 部署后页面显示404错误

A: 检查以下几点：
- `astro.config.mjs` 中的 `site` URL 是否正确
- 如果使用了 `base` 路径，确保所有内部链接都正确处理
- GitHub Pages 设置中的分支和目录是否正确

### Q: 网站样式没有加载

A: 检查：
- 浏览器开发者工具中的 Console 是否有错误
- CSS 文件的路径是否正确（特别是使用了 `base` 路径时）
- 清空浏览器缓存并重新加载

### Q: 如何自定义域名

A: 
1. 在项目根目录 `public/` 文件夹中创建 `CNAME` 文件
2. 在文件中添加你的自定义域名，例如 `worldcollege.com`
3. 推送到 GitHub
4. 在你的域名注册商处配置 DNS 记录指向 GitHub Pages

## 本地开发

如果需要在本地测试，运行：

```bash
# 开发服务器
npm run dev

# 访问 http://localhost:3000
```

## 支持

如有问题，请提交 GitHub Issue 或通过邮件联系。

---

**最后更新**: 2024年7月
