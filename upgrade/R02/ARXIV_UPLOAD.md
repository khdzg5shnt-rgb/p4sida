# P4 arXiv预印本文件与填写信息

2026-10-10（北京时间）。基线main：`0fbaacbe9a96466082e88accf292298b3412235f`。已准备文件，未提交。

## 上传与元数据

上传 `P4_ARXIV_SOURCE.zip`，根目录只有 `P4_ARXIV.tex`。也可单独上传同一TeX，二者选一种；编译器为PDFLaTeX。参考文献内嵌，无外部图片或本地宏包依赖。`P4_ARXIV.pdf` 是由该ZIP解压出的源码独立编译所得的43页预览。源码包不含PDF、日志、辅助文件、历史稿或研究记录；本说明也不进入上传包。

- Title: `Sparse Observations and Pattern Complexity of Safe Feedbacks`
- Authors: `Ziqing Ding (School of Mathematical Sciences, Nanjing Normal University)`
- 建议主分类：`math.DS`（Dynamical Systems）；按本文内容可考虑交叉分类 `math.OC`（Optimization and Control）。这是内容匹配建议，未替作者选择。
- Comments: `43 pages`
- MSC-class: `93C55, 37B10, 37B40, 94A17`
- Journal-ref、DOI、Report-no：本轮没有相应信息，留空。
- Abstract：复制下段，与论文摘要相同，仅合并换行，共1175个ASCII字符。

```text
A safe state feedback generates a sequence of control instructions from each initial state. We study the growth of the number of patterns seen at selected times, with a fixed control period $\tau$. The main question is whether one observation sequence detects complexity uniformly over all safe Borel feedbacks. We answer it when all legal blocks have a common endpoint map conjugate to a power of a mixing one-sided shift of finite type. The minimum rate is $\log r/\tau$, where $r$ is the minimum number of block safety domains covering the state space, and every observation sequence with diverging gaps attains it. When controls have different successors, we bound the initial-state sets producing specified words by products of inverse-transfer operators. A contraction condition, combined with the finite covering lemma of Kerr and Li, determines the minimum maximal-pattern entropy; the observation times in this argument may depend on the feedback. A separate deletion argument gives common attaining sequences for countably many name languages. Symbolic and affine examples distinguish these conclusions from finite-horizon safe covering and from invariance entropy.
```

账号联系方式、许可选项和提交协议由作者在arXiv页面填写或确认。arXiv会再次编译源码；提交前须查看平台生成的PDF及元数据，本地检查不能代替平台预览。

官方依据（2026-10-10核查）：[TeX/LaTeX提交](https://info.arxiv.org/help/submit_tex.html)、[元数据字段](https://info.arxiv.org/help/prep.html)、[分类](https://arxiv.org/category_taxonomy)、[生成式AI说明](https://info.arxiv.org/help/moderation/index.html#policy-for-authors-use-of-generative-ai-language-tools)。

## 本轮改动与核对

作者确认丁子卿独著、南京师范大学数学科学学院，当前没有目标期刊，先准备arXiv，并表示已检查现稿。英文署名和单位原本相符，直接保留。没有加入邮箱、ORCID、基金、利益冲突或致谢的空白栏目。

实际论文差异只有两处：去掉日期栏；AI说明缩为一段，仍明确包含数学探索、候选证明、原始文献比较与文稿准备。没有写成“仅语言润色”，也未增加最终文件已获作者审阅或外部评审的声明。旧的模型版本不可追溯说明保留在历史稿中。

摘要、引言、所有定义、定理、证明、附录及11项参考文献与基线逐字一致。本轮是预印本整理和文件检查，没有宣称新做一轮全稿证明审查；数学范围和未解问题不变，见现稿第8节及 `FINAL_READER_CHECK.md`。

ZIP独立解压后，以禁用shell escape的PDFLaTeX（本地TeX Live 2023）编译。最终43页，无警告、未定义引用或Overfull/Underfull。157标签及编号、34编号结果、31proof保持。全部43页已查看；仅第1页日期和第42页AI段落有渲染变化，其余41页与基线逐像素相同。无空白页、越界文字、替代字符或无效内部页跳转。尚未在arXiv服务器编译。

原稿及历史稿、研究记录保留；2002b保持“未取得、未核实，获取关闭”。原稿SHA-256仍为 `c38552174b2fb0dee04ed56038952437f3e3ec3bd3725a5b1ace7812703f81ed`。

| 文件 | 字节数 | SHA-256 |
|---|---:|---|
| `P4_ARXIV.tex` | 163488 | `8729a7b9dfd5f00052c2095bb9a02ff4049579d4b70c9ba43245798eb6f49487` |
| `P4_ARXIV.pdf` | 587795 | `019a79da9b66f31c44d542f8b3cd53a3fdb2fc2a69b85df1a1c0c4f9c719ba99` |
| `P4_ARXIV_SOURCE.zip` | 58388 | `e8af56a89518ade19ea16133ec9e3c8a18fd695d950b1c8c100b854f71505f81` |
