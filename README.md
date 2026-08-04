# liuyu 个人学术主页

经典极简学术风（风格 A）：纯 HTML + CSS，零依赖、无构建步骤。

## 文件结构

```
liuyu_profile/
├── index.html                      # 主页全部内容（所有占位处都有 <!-- TODO --> 注释）
├── style.css                       # 样式
├── assets/
│   ├── photo-placeholder.svg       # 照片占位图 → 换成真实 photo.jpg
│   ├── pubs/thumb-placeholder.svg  # 论文缩略图占位 → 每篇论文一张图
│   └── cv.pdf                      # （待放入）简历 PDF
└── README.md
```

## 本地预览

直接双击 `index.html`，或：

```bash
cd liuyu_profile && python3 -m http.server 8000
# 浏览器打开 http://localhost:8000
```

## 替换真实内容

在 `index.html` 里搜索 `TODO`，逐项替换：

1. 姓名（`<title>` 和 `<h1>`，英文 + 中文）
2. Bio 两段（研究方向 + 单位/实验室）
3. 链接行：Email / Google Scholar / GitHub / CV 的真实地址
4. 照片：把 `assets/photo.jpg` 放进去，`<img class="portrait">` 的 `src` 改为 `assets/photo.jpg`
5. News 条目（不需要可整段删除）
6. Publications：每篇论文一个 `.pub` 块，复制粘贴即可；缩略图放 `assets/pubs/`
7. Education & Experience 列表
8. Footer 更新日期

## 部署到 GitHub Pages（3 步）

1. 在 GitHub 新建仓库，命名为 `<你的用户名>.github.io`（公开仓库）
2. 把本目录内容 push 上去：

   ```bash
   cd liuyu_profile
   git init && git add -A && git commit -m "personal homepage"
   git branch -M main
   git remote add origin git@github.com:<你的用户名>/<你的用户名>.github.io.git
   git push -u origin main
   ```

3. 仓库 Settings → Pages → Source 选 `main` 分支根目录（通常自动开启）。
   几分钟后访问 `https://<你的用户名>.github.io` 即可。
