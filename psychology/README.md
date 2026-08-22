# 手机版课程包（export/）

这个目录是**手机友好版本**，与 lessons/ 下原始版本的区别：

- lessons/*.html（原始版）：引用外部样式/脚本，适合电脑浏览器从工作区打开。
- export/lessons/*.html（自包含版）：样式和测验脚本全部内嵌，**单个文件即可在任何浏览器打开**，手机上体验良好（响应式排版 + 触屏测验）。

## 在手机上查看的三种方式

### 方式 A：托管后发链接（体验最佳）
1. 把整个 export/ 目录上传到任意静态托管（GitHub Pages、Gitee Pages、Vercel、Netlify 等）。
2. 得到网址后（如 https://yourname.github.io/psychology/），把链接发到飞书群即可。
3. 群里消息由 `10_Projects/课程推送/` 的脚本自动发"摘要 + 链接"。

### 方式 B：直接把 HTML 文件传到飞书群（无需托管）
1. 把 export/lessons/0001-*.html 等文件作为附件上传到飞书群。
2. 手机上下载后用浏览器打开即可（测验可交互）。

### 方式 C：粘贴文字摘要（最轻量）
把 export/summaries/lesson-*.txt 的内容粘贴到群里或飞书云文档。

## 新增课程后需要做什么
1. 在 lessons/ 写好原始版课程。
2. 让老师生成自包含版（复制到 export/lessons/）和文字摘要（export/summaries/）。
3. 若用方式 A：把新文件上传到托管空间；若用方式 B：把新文件传到群里。
4. 推送摘要和链接：由 `10_Projects/课程推送/` 统一处理（脚本 + 配置在那里，四门课共用）。
