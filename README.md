# courses · 课程手机版（GitHub Pages）

四门学习课程的手机友好版，由 `E:\KnowledgeBase` 的课程目录生成，通过 GitHub Pages 公开访问。

## 课程与网址

| 课程 | 子目录 | 页面网址 |
| --- | --- | --- |
| 心理学 | `psychology/` | https://278143.github.io/course/psychology/ |
| 考研 | `kaoyan/` | https://278143.github.io/course/kaoyan/ |
| FQ（理财） | `fq/` | https://278143.github.io/course/fq/ |
| 法律 | `law/` | https://278143.github.io/course/law/ |

课程链接形如：https://278143.github.io/course/psychology/lessons/0001-psychology-as-science.html

## 如何更新

1. 在 `20_Areas/<课程>/lessons/` 写好原始课程；
2. 运行 `make-export.ps1` 生成自包含版到 `export/`，并编写 `export/summaries/` 文字摘要；
3. 把 `export/` 内容同步到本仓库对应子目录；
4. `git add . && git commit -m "新增第 N 课" && git push`；
5. 等 1-2 分钟 Pages 更新，再运行 `10_Projects/课程推送/` 的推送脚本，群里消息即带链接。

## 注意

- 本仓库**公开**：只放课程内容，不要把含 webhook 的配置文件放进来。
- `.nojekyll`：禁用 Jekyll，保证文件按原样托管。
