# 部署到 GitHub Pages（手机端访问完整课程）

## 先回答你的问题

**"是需要提交到远程仓库吗？"** —— 是的。GitHub Pages 的运作方式：把文件放进一个 GitHub 仓库（远程仓库），GitHub 自动生成一个网址（形如 `https://你的用户名.github.io/psychology/`），手机浏览器打开这个网址就能访问完整课程。

**"网站是我自用"** —— 完全没问题。注意一点：GitHub Pages 免费版只支持**公开仓库**，这意味着"知道网址的人"都能打开（网址是随机性很强的长地址，不会被搜索引擎收录，别人几乎不可能找到）。课程内容只是你的学习笔记，公开一个随机网址风险很低。
如果你希望彻底私有（不想公开仓库），有两个替代方案：
- **不用托管**：把 export/lessons/ 下的 HTML 文件直接传到飞书群，手机下载后用浏览器打开（同样可交互）——完全私有。
- **Cloudflare Pages**：免费，支持从私有仓库构建，但部署出来的网址本身仍是公开可访问的。

## 推荐方案：公开仓库 + GitHub Pages

### 方式 1：网页上传（最简单，无需 git 命令）
1. 打开 https://github.com/new ，仓库名填 `psychology`，选 Public，勾选 "Add a README file"，创建。
2. 进入仓库 → 点 "Add file" → "Upload files"。
3. 把本地 `export\` 目录里的 **lessons、reference、summaries 三个文件夹和 README.md** 拖进去上传（注意保留目录结构：lessons/0001-xxx.html 等）。
4. 上传后点 "Commit changes"。
5. 仓库页 → "Settings" → 左侧 "Pages" → Source 选 "Deploy from a branch" → Branch 选 main + / (root) → Save。
6. 等 1-2 分钟，出现网址 `https://你的用户名.github.io/psychology/`。
7. 测试：手机浏览器打开 `https://你的用户名.github.io/psychology/lessons/0001-psychology-as-science.html` 应能看到课程。

### 方式 2：git 命令行（后续更新更快）
```bash
cd E:/KnowledgeBase/20_Areas/psychology
git init
git add export
git commit -m "psychology lessons"
git branch -M main
git remote add origin https://github.com/你的用户名/psychology.git
git push -u origin main
# 然后同上：Settings -> Pages -> Deploy from branch: main / (root)
```

## 之后

- 拿到网址后，把它发给老师（我会填入 feishu-config.json 的 baseUrl）。
- 之后每次发课：把新文件放进 export/，重新 push（或网页上传），再运行同步脚本——群里消息就会带上"打开完整课程"的链接。
