# P4：闭覆盖、采样与全部 Borel 安全反馈

仓库 khdzg5shnt-rgb/p4sida。近期争取真实新意、独立发表及一区投稿依据，后续一区 Top，长期 Annals、Inventiones、JAMS、Acta。不认证或保证升级。数学攻坚、选刊、投稿准备及实际投稿保持暂停。

- [当前结果与准确停点](CURRENT.md)
- [完整核验；第45节为跨层延拓反例](upgrade/R02/VERIFICATION.md)
- [十篇四大论文学习与适用限制](upgrade/R02/FOUR_MAJOR_STUDY.md)
- [下一步边界](upgrade/R02/NEXT_COMMAND.md)
- [候选TeX](upgrade/R02/P4_REVISED.tex)/[PDF](upgrade/R02/P4_REVISED.pdf)
- [R02研究](upgrade/R02/RESEARCH.md)/[R01历史](upgrade/R01/RESEARCH.md)

## 最新完整结果

基线 main 79fbcdf846b8cd00394f62e8bc7b2b9177852121。第45节实际检验跨层规则：先确定真实轨道编码，再加入新状态，碰到已有轨道时继承尾串，并保持旧控制。已给出完整反例，否定一般延拓接口。

种子为 w=1010001101 的安全真实十周期及端点0、6。其全部名字在第42节固定 Y 中，已有域上的投影和单步一致性均成立。但新状态6808/5275只能取0，随后进入10212/5275，强迫接上 e=(0100011011)∞；e∈Y而0e∉Y，全部十相位已排除。

即使在种子外任意大范围改控，也不能修复保留这个种子的反馈。这只排除特定不可撤回延拓入口，不排除其他种子或所有 Borel 实现。初始化还须处理强制逆前驱及路径合流，现无完整全域构造。

## 数值与适用边界

保持
$$
\log(3/2)\le\ell_2\le\ell_2^A\le\log\rho,\qquad
h_{A_2}(s_g)=\log\rho,
$$
ρ⁶=ρ⁵+ρ⁴+ρ+1。两上界本轮下降量均为0，贪心最优性、精确值及达到者未决定；M₁=log2、log(3/2)≤L₁≤log2及一般问题不变。

第17节闭覆盖、全部 Borel 细化和预设渐疏采样公式、共同后继应用及第18节边界保留。第42节 Y 的抽象低熵仍未实现；第43节阈值等入口排除及第44节十篇研读完整保留。

本轮新增了具体兼容性反例，没有实际数值改善或可推广构造判据，也没有新增足够独立成篇或一区投稿依据。历史覆盖未裁决，不认证原创性。尝试已结束，恢复暂停，不自动换种子继续。

## 文献、历史与保留

本轮从已读三篇原文定向补核跨层兼容、互斥编码及动力一致标记，精确定位和 APA/DOI见第45节。没有直接套用缺少前提的文献定理。HMY归属保留；2002b仍未取得、未核实，获取关闭，不索取、不循环、不替代。其他暂停分支不重开。

VERIFICATION第1–44节原554,178字节与十份保留文件不变。候选稿 Sparse Sampling and Borel Refinements of Closed Covers 的TeX/PDF、[投稿信](upgrade/R02/COVER_LETTER_DRAFT.md)、[作者声明](upgrade/R02/AUTHOR_DECLARATIONS_DRAFT.md)、[投稿清单](upgrade/R02/SUBMISSION_CHECKLIST.md)不改或外发。

原稿SHA-256：c38552174b2fb0dee04ed56038952437f3e3ec3bd3725a5b1ace7812703f81ed。

仅更新四份记录，提交后按实际SHA全文回读十四份更新及保留文件，核验历史前缀和散列。只处理P4，不开R03、不恢复增长分类、不改其他项目、不自动改写候选稿。
