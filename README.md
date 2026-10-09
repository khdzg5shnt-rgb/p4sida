# P4：Sparse Sampling and Inverse Capacity in Safe Feedback Systems

**现行主要阅读版本：完整数学核验和五篇JDE全文对照后的56页英文结构审阅稿。** 本轮基线main为`32aebfe608aeb818c8ab1eb46360d60d8dca0846`。主定理、假设和数值不变；正文重新组织为11节，全部旧稿保留。

- [现行PDF](upgrade/R02/P4_STYLE_REVIEWED.pdf) / [TeX](upgrade/R02/P4_STYLE_REVIEWED.tex)
- [完整数学核验、五篇原文对照、实际修改和逐项内容去向](upgrade/R02/P4_MATH_STYLE_REVIEW.md)
- [当前状态](CURRENT.md) / [后续停点](upgrade/R02/NEXT_COMMAND.md)
- [核验历史，最新第70节](upgrade/R02/VERIFICATION.md)
- [60页选择补回稿](upgrade/R02/P4_SELECTED_REVIEWED.pdf) / [TeX](upgrade/R02/P4_SELECTED_REVIEWED.tex) / [当时取舍报告](upgrade/R02/CONTENT_SELECTION_REVIEW.md)
- [全历史覆盖索引](upgrade/R02/CONTENT_COVERAGE_AUDIT.md) / [历史manifest](upgrade/R02/CONTENT_COVERAGE_MANIFEST.json)

主线为：安全逆容量产品收缩给全部合法Borel反馈的最大模式阈值；共同后继的闭覆盖定理给共同渐疏采样的精确值；可数语言提供另一共同达到条件。有限柱机制和具体反馈例说明这些结果如何使用，附录解释实现、返回、切换及概率方法的边界。

独立复核60页稿全部43项定理类结果、6个例子及未编号推导后，重写摘要、引言和衔接；将纯组合反例移到G.1，核层和嵌套可行链工具留在旧稿与研究记录，保留周期种子所需相位判据。现稿42项定理类结果、6个例子，197标签，12项文献；全部56页和编译检查完成，无未定义引用或排版警告。未发现需更改主定理或数值的实质错误，未识别出保留已证声明的未修复缺口；不等于作者或外部同行确认。

五篇对照均核实正式发表于JDE并完整阅读，其中两篇为出版版、三篇为作者公开全文，后三篇最终出版版尚未逐字核对。具体页码、版本、DOI及写作改动见报告。AI说明和数学工具归属保留，不声称已达发表标准、不虚构AI率。

## 保留版本和记录

- [54页补全PDF](upgrade/R02/P4_COMPLETE_REVIEWED.pdf) / [TeX](upgrade/R02/P4_COMPLETE_REVIEWED.tex) / [当时覆盖审查](upgrade/R02/CONTENT_COVERAGE_AUDIT.md)
- [47页审阅PDF](upgrade/R02/P4_REVIEWED.pdf) / [TeX](upgrade/R02/P4_REVIEWED.tex) / [当时审查](upgrade/R02/MANUSCRIPT_REVIEW.md)
- [48页整合PDF](upgrade/R02/P4_INTEGRATED.pdf) / [TeX](upgrade/R02/P4_INTEGRATED.tex) / [当时整合说明](upgrade/R02/INTEGRATION_NOTES.md)
- [原稿](original/P4_FINAL.tex)
- [九页候选TeX](upgrade/R02/P4_REVISED.tex) / [PDF](upgrade/R02/P4_REVISED.pdf)
- [R02研究](upgrade/R02/RESEARCH.md) / [R01研究](upgrade/R01/RESEARCH.md)
- [十篇论文学习记录](upgrade/R02/FOUR_MAJOR_STUDY.md)
- [原候选投稿信](upgrade/R02/COVER_LETTER_DRAFT.md) / [声明草稿](upgrade/R02/AUTHOR_DECLARATIONS_DRAFT.md) / [清单](upgrade/R02/SUBMISSION_CHECKLIST.md)


本轮新增3份文件、更新4份文件；其余24份基线文件保持字节和Git blob。VERIFICATION只追加第70节，原1–69节938,458字节不改。原稿SHA-256仍为`c38552174b2fb0dee04ed56038952437f3e3ec3bd3725a5b1ace7812703f81ed`。提交后以实际SHA回读全部31份文件，并核验父提交、树和main，最终SHA随交付给出。

一般共同采样、原系统精确L₁与偶数优化、Y/H实现、一般满支撑标量化、返回抽取及无限可行链等仍未解决，不自动续攻。2002b保持“未取得、未核实，获取关闭”。仅P4/R02，无R03、增长分类、选刊、投稿、联系他人或代理分派。
