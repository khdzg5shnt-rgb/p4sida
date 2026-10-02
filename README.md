# P4：Sparse-Time Complexity of Invariant Control Languages

这是 `khdzg5shnt-rgb/p4sida` 的 P4 研究仓库。目标是研究能否形成面向 Annals of Mathematics、Inventiones Mathematicae、Journal of the American Mathematical Society、Acta Mathematica 的重大贡献；不以润色、扩写或普通投稿整理替代，不承诺成功。

唯一原稿为 [`original/P4_FINAL.tex`](original/P4_FINAL.tex)，逐字保留，SHA-256 为 `c38552174b2fb0dee04ed56038952437f3e3ec3bd3725a5b1ace7812703f81ed`。所有升级研究保存于 `upgrade/`，不覆盖原稿。

- [当前状态](CURRENT.md)
- [R02 停点核验、独立证明、新增原文及未核实项](upgrade/R02/VERIFICATION.md)
- [R02 有限控制化简、四控制共同达到障碍及原始研究历史](upgrade/R02/RESEARCH.md)
- [R01 原稿审查、文献、数学结果与路线判断](upgrade/R01/RESEARCH.md)
- [下一条增量核验指令](upgrade/R02/NEXT_COMMAND.md)

R01 纠正固定周期模式下确界的达到性，并给出自治紧致指定策略族的 minimax 反例及其混合反馈限制。R02 证明同控制块原子合并的精确化简，并构造四控制系统：普通不变熵为零，周期一全部 Borel 数值 minimax 两侧均为 `log 2`；指定子族有严格缺口，逐策略共同达到失败。这排除较强的证明桥梁，没有否定一般全类数值问题。

停点核验从定义复核上述两项 R02 证明，均通过；全部安全选择器及任意 Borel 混合已纳入。补写了有限模式闭包、模式增长极限和稀疏生成族闭性的细节，未发现改变数值结论的错误。新取得一份 2002a 早期作者稿相关正文，并定位旧 Toeplitz 证明的修正线索；关键最终原文仍有缺口，原创性未认证。

当前保持这条四大升级路线及整篇重写的暂停：一般数值问题未决定，没有新的通用机制或重大结构后果依据。后续只做有新材料的定向增量，不自动开 R03，不恢复增长分类，不增加第三路线，不降低目标，不修改其他论文或仓库。
