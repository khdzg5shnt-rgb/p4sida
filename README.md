# P4：Sparse Observations and Pattern Complexity of Safe Feedbacks

**现行阅读版本：面向专业读者实质重写后的52页英文稿。** 本轮基线main为`6f137a1557b7650a2c3a09ead6047f6ed82174c9`。导师反馈促成本次重新组织，旧报告的“可以停止修改”判断不再作为当前写作评价。

- [现行PDF](upgrade/R02/P4_REWRITTEN.pdf) / [TeX](upgrade/R02/P4_REWRITTEN.tex)
- [改写报告：内容去向、数学核验、五处前后对照及JDE比较](upgrade/R02/READABILITY_REWRITE.md)
- [当前状态](CURRENT.md) / [后续恢复说明](upgrade/R02/NEXT_COMMAND.md)
- [核验历史，最新§72](upgrade/R02/VERIFICATION.md)
- [保留的57页稿](upgrade/R02/P4_FINAL_REVIEWED.pdf) / [TeX](upgrade/R02/P4_FINAL_REVIEWED.tex) / [旧终审报告](upgrade/R02/FINAL_PAPER_REVIEW.md)
- [56页稿](upgrade/R02/P4_STYLE_REVIEWED.pdf) / [TeX](upgrade/R02/P4_STYLE_REVIEWED.tex) / [历史报告](upgrade/R02/P4_MATH_STYLE_REVIEW.md)
- [60页稿](upgrade/R02/P4_SELECTED_REVIEWED.pdf) / [TeX](upgrade/R02/P4_SELECTED_REVIEWED.tex) / [当时取舍报告](upgrade/R02/CONTENT_SELECTION_REVIEW.md)
- [全历史覆盖索引](upgrade/R02/CONTENT_COVERAGE_AUDIT.md) / [历史manifest](upgrade/R02/CONTENT_COVERAGE_MANIFEST.json)

从已有三符号系统出发，先解释实际名字、采样归一化和两个优化顺序。共同后继公式在前，改变后继的反例引出容量定理；矩阵检验移附录，完整名字框架延后，经典比较与符号分离合并。长证明补步骤理由，五个不参与现行证明的辅助结果留在旧稿；具体范围与依赖见改写报告。

主定理和数值不变。阈值2处端点措辞、移动后的首次定义及回指已修正，受影响证明重新核验。实际编译并查看全部52页，188标签和12项文献解析，无编译/版式警告。AI说明和参考文献原样保留。复用五篇JDE全文，区分两篇出版版与三篇作者稿，不据此宣称读者已认可或达到发表标准。

技术附录仍需专业细读，尚无独立试读反馈；共同采样、精确L₁/偶采样优化、贪心最优性及一般参考概率等数学问题没有解决。2002b保持“未取得、未核实，获取关闭”。

## 保留版本和记录

- [54页补全PDF](upgrade/R02/P4_COMPLETE_REVIEWED.pdf) / [TeX](upgrade/R02/P4_COMPLETE_REVIEWED.tex) / [当时覆盖审查](upgrade/R02/CONTENT_COVERAGE_AUDIT.md)
- [47页审阅PDF](upgrade/R02/P4_REVIEWED.pdf) / [TeX](upgrade/R02/P4_REVIEWED.tex) / [当时审查](upgrade/R02/MANUSCRIPT_REVIEW.md)
- [48页整合PDF](upgrade/R02/P4_INTEGRATED.pdf) / [TeX](upgrade/R02/P4_INTEGRATED.tex) / [当时整合说明](upgrade/R02/INTEGRATION_NOTES.md)
- [原稿](original/P4_FINAL.tex)
- [九页候选TeX](upgrade/R02/P4_REVISED.tex) / [PDF](upgrade/R02/P4_REVISED.pdf)
- [R02研究](upgrade/R02/RESEARCH.md) / [R01研究](upgrade/R01/RESEARCH.md)
- [十篇论文学习记录](upgrade/R02/FOUR_MAJOR_STUDY.md)
- [原候选投稿信](upgrade/R02/COVER_LETTER_DRAFT.md) / [声明草稿](upgrade/R02/AUTHOR_DECLARATIONS_DRAFT.md) / [清单](upgrade/R02/SUBMISSION_CHECKLIST.md)

本轮新增3份、更新4份，其余30份基线文件保留。VERIFICATION仅追加§72，前950193字节不改。原稿SHA-256仍为`c38552174b2fb0dee04ed56038952437f3e3ec3bd3725a5b1ace7812703f81ed`。提交使用main复核和expected_sha保护，提交后按实际SHA回读全部37份文件并核父提交、树和main，实际结果随交付给出。仅P4/R02，无代理、新研究、选刊、投稿或联系他人。
