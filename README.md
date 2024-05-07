# 江南大学博士学位论文Latex模版
在zhuangbo同学模版的基础上就行了修改，能够在windows11 和 macOS上运行，主要更改内容包括：
1. 修改了macOS的默认字体，使其能够运行
2. 修改了jnthesis.cls的样式，使其能够支持算法伪代码书写

最近修改日期：2024/5/7

如果其他问题，欢迎在PR中提出。

以下为原作者的使用指南，供参考：
---
原始地址：https://gitee.com/zhuangbo/jnthesis

文档类 `jnthesis.cls` 基于 `ctex` 宏包定义了论文格式，包括字体，字号，行距，标题，页眉，页脚，目录，摘要，正文等各种格式。

文件 `jn.bst` 定义了参考文献格式。

推荐使用 TeXlive 发行版，不推荐使用 CTEX 发行版。

为便于编辑，通常将长文档分成若干文件。本论文模板还提供了以下文件：

| 文件                            | 说明                                        |
| ------------------------------- | ------------------------------------------- |
| `root.tex`                      | 主文档，整个文档结构，用 XeLaTeX 编译此文档 |
| `main.tex`                      | 主要内容，包含主要章节内容                  |
| `cover.doc`                     | 封面，DOC 文件，修改编辑后另存为 PDF        |
| `cover.pdf`                     | 封面，PDF 文件，插入文档                    |
| `statement.doc`                 | 声明和授权，DOC 文件，修改编辑后另存为 PDF  |
| `statement.pdf`                 | 声明和授权，PDF 文件，插入文档              |
| `setup/settings.tex`            | 用户设置，如：标题，作者，其他宏包和样式等  |
| `setup/userdefs.tex`            | 用户自定义符号                              |
| `preface/e_abstract.tex`        | 英文摘要和英文关键词                        |
| `preface/c_abstract.tex`        | 中文摘要和中文关键词                        |
| `body/*.tex`                    | 各章节内容，不需要时在 main.tex 中删除      |
| `appendix/acknowledgements.tex` | 致谢                                        |
| `appendix/publications.tex`     | 发表论文                                    |
| `references.bib`                | 参考文献数据库                              |
| `figures/...`                   | 插图                                        |

具体用法如下：

1. 打开 `root.tex` 文件，设置文档参数以指定博士 (`doctor`)，硕士 (`master`) 或毕业(`nodegree`) 论文。

2. 打开 `main.tex` 文件，规划论文主要章节。不需要的章节可以删除或注释掉。

3. 修改 `cover.doc` 文件生成封面 `cover.pdf`。

4. 修改 (如有必要) statement.doc` 生成 `statement.pdf`。

5. 修改 `setup/settings.tex` 设置标题，作者，包含其他宏包等其他设置。

6. 修改 (如有必要) `setup/userdefs.tex` 添加用户自定义符号或命令。

7. 修改 `preface/e_abstract.tex` 添加英文摘要和英文关键词。

8. 修改 `preface/c_abstract.tex` 添加中文摘要和中文关键词。

9. 修改 `body/ch01.tex` 等，撰写各章内容。

10. 修改 `appendix/acknowledgements.tex` 添加致谢内容。

11. 修改 `appendix/publications.tex` 添加发表论文。

12. 修改任何内容后，用 XeLaTeX 编译 `root.tex` 文件得到最终论文 `root.pdf`。若参考文献不正确，首先执行 BibTeX，再多次 (三次以上) 执行 XeLaTeX，直到得到正确的参考文献.

一次完整的编译过程为 XeLaTeX > BibTeX > XeLaTeX > XeLaTeX > XeLaTeX。 通常在引用参考文献没有发生变化时，仅需要执行一次 XeLaTeX。 由于已经把整个文档划分成多个文件，加快了编译速度。 当 bib 文献数据库或文献引用发生变化时，为确保最终内容正确，可以执行一遍完整的编译过程。

本模板采用 MIT 协议授权，如有不完善之处请自行修改代码。
