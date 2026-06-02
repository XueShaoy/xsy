# Shaoyang 的个人主页

基于 [Hugo](https://gohugo.io/) + [LoveIt](https://github.com/dillonzq/LoveIt) 主题搭建，通过 GitHub Actions 自动部署到 GitHub Pages。

🔗 在线地址：<https://xueshaoy.github.io/xsy/>

## 环境要求

- [Hugo Extended](https://gohugo.io/installation/) `>= 0.146.0`（本项目使用 0.162.1）

## 本地预览

```bash
# 首次克隆需要拉取主题子模块
git clone --recursive https://github.com/XueShaoy/xsy.git
# 或克隆后执行
git submodule update --init --recursive

# 启动本地服务器（含草稿）
hugo server -D
```

浏览器访问 <http://localhost:1313/xsy/>。

## 写作

新建文章：

```bash
hugo new posts/我的文章/index.md
```

文章默认 `draft: true`，发布前改为 `draft: false`。

## 目录结构

```
.
├── content/          # 内容（文章、关于页）
│   ├── about/        # 关于页面
│   └── posts/        # 文章
├── static/           # 静态资源（图片等）
├── themes/LoveIt/    # 主题（git submodule）
├── hugo.toml         # 站点配置
└── .github/workflows/deploy.yml  # 自动部署
```

## 部署说明

推送到 `main` 分支后，GitHub Actions 会自动构建并部署。

⚠️ 首次使用需在仓库 **Settings → Pages → Build and deployment → Source** 中选择 **GitHub Actions**。

## 自定义

- 头像：替换 `static/images/avatar.svg`（或改为自己的 `avatar.png` 并更新 `hugo.toml`）
- 站点信息 / 菜单 / 社交链接：编辑 `hugo.toml`
