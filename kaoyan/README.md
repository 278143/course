# 手机版课程包（export/）

这个目录是**手机友好版本**，与 lessons/ 下原始版本的区别：

- lessons/*.html（原始版）：引用外部样式/脚本，适合电脑浏览器从工作区打开。
- export/lessons/*.html（自包含版）：样式和测验脚本全部内嵌，**单个文件即可在任何浏览器打开**，手机上体验良好。

## 在手机上查看

- 本目录已部署到 GitHub Pages（随 10_Projects/课程推送/ 项目统一发布）。
- 更新内容后重新运行生成脚本（make-export.ps1），再推送到公开仓库即可。

## 目录

- lessons/ 自包含课程页
- summaries/ 文字摘要（推送用）
- reference/ 参考页
- MISSION.md / NOTES.md / RESOURCES.md 课程文档