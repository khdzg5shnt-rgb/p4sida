# P4：Sparse Sampling and Inverse Capacity in Safe Feedback Systems

**现行主要阅读版本：终审后的57页英文稿。** 本轮基线main为`cf1f8582ecb404535cca8e5bfbe225e27319388b`。全文已形成明确问题、两条证明路线、应用和边界反例相衔接的研究论文组织。

- [现行PDF](upgrade/R02/P4_FINAL_REVIEWED.pdf) / [TeX](upgrade/R02/P4_FINAL_REVIEWED.tex)
- [完整终审报告：数学发现、五篇JDE原文对照、修订及停点](upgrade/R02/FINAL_PAPER_REVIEW.md)
- [当前状态](CURRENT.md) / [后续停点](upgrade/R02/NEXT_COMMAND.md)
- [核验历史，最新第71节](upgrade/R02/VERIFICATION.md)
- [保留的56页结构稿](upgrade/R02/P4_STYLE_REVIEWED.pdf) / [TeX](upgrade/R02/P4_STYLE_REVIEWED.tex) / [历史报告](upgrade/R02/P4_MATH_STYLE_REVIEW.md)
- [60页选择补回稿](upgrade/R02/P4_SELECTED_REVIEWED.pdf) / [TeX](upgrade/R02/P4_SELECTED_REVIEWED.tex) / [当时取舍报告](upgrade/R02/CONTENT_SELECTION_REVIEW.md)
- [全历史覆盖索引](upgrade/R02/CONTENT_COVERAGE_AUDIT.md) / [历史manifest](upgrade/R02/CONTENT_COVERAGE_MANIFEST.json)

主线保持：安全逆容量产品给全部合法Borel反馈的最大模式阈值；共同后继的闭覆盖定理给预给渐疏采样的精确值；可数语言提供另一共同达到条件。正文11节与8个附录分工保持，六组补回内容按原具体用途保留，没有新增数学成果或再次大规模搬移。

本轮连续读完现稿全部论证并复核关键依赖。实际修正平滑例未解问题的两项容量和条件、周期种子的两A范围、碰撞密度设置的非零斜率及空窗口说明；主定理及数值不变。补问题动机，删少量审计口吻和重复过渡。没有识别出保留已证结论的未修复证明缺口；这不是作者确认、形式化证明或同行审定。

五篇已核JDE全文复用并按问题重读：两篇出版版、三篇作者稿，后三篇最终出版版未逐字校核。具体位置和修改见终审报告。旧P4_MATH_STYLE_REVIEW四条摘要误述在新报告§2.3勘误，历史文件保留。

实际编译57页，197标签及所有编号保持，48个编号结果、43个proof环境和12项文献保留；全部页面已检查，引用均解析，无编译或版式警告。AI说明和工具归属保留。不提供AI检测率或JDE发表保证。

## 保留版本和记录

- [54页补全PDF](upgrade/R02/P4_COMPLETE_REVIEWED.pdf) / [TeX](upgrade/R02/P4_COMPLETE_REVIEWED.tex) / [当时覆盖审查](upgrade/R02/CONTENT_COVERAGE_AUDIT.md)
- [47页审阅PDF](upgrade/R02/P4_REVIEWED.pdf) / [TeX](upgrade/R02/P4_REVIEWED.tex) / [当时审查](upgrade/R02/MANUSCRIPT_REVIEW.md)
- [48页整合PDF](upgrade/R02/P4_INTEGRATED.pdf) / [TeX](upgrade/R02/P4_INTEGRATED.tex) / [当时整合说明](upgrade/R02/INTEGRATION_NOTES.md)
- [原稿](original/P4_FINAL.tex)
- [九页候选TeX](upgrade/R02/P4_REVISED.tex) / [PDF](upgrade/R02/P4_REVISED.pdf)
- [R02研究](upgrade/R02/RESEARCH.md) / [R01研究](upgrade/R01/RESEARCH.md)
- [十篇论文学习记录](upgrade/R02/FOUR_MAJOR_STUDY.md)
- [原候选投稿信](upgrade/R02/COVER_LETTER_DRAFT.md) / [声明草稿](upgrade/R02/AUTHOR_DECLARATIONS_DRAFT.md) / [清单](upgrade/R02/SUBMISSION_CHECKLIST.md)


本轮新增3份、更新4份文件，其余27份基线文件保持字节和Git blob。VERIFICATION只追加第71节，原943930字节不改。原稿SHA-256仍为`c38552174b2fb0dee04ed56038952437f3e3ec3bd3725a5b1ace7812703f81ed`。提交使用实际main和expected_sha lease，提交后按实际SHA回读全部34份文件并核父提交、树和main；实际SHA随交付提供。

一般共同采样、原系统精确L₁/偶采样优化、Y/H实现、一般满支撑标量化、返回抽取及无限可行链等仍未解决，不自动续攻。已清楚的结构、证明和必要限制应停止机械修改；贡献强度与成果取舍留给作者判断，不默认再开同类审查。2002b保持“未取得、未核实，获取关闭”。仅P4/R02，无P3/P6读改、代理分派、新研究、R03、增长分类、选刊、投稿或联系他人。
