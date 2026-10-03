# P4：Sparse-Time Complexity of Invariant Control Languages

这是 `khdzg5shnt-rgb/p4sida` 的 P4 研究仓库。目标是研究能否形成面向 Annals of Mathematics、Inventiones Mathematicae、Journal of the American Mathematical Society、Acta Mathematica 的重大贡献；不以润色、扩写或普通投稿整理替代，不承诺成功。

唯一原稿为 [`original/P4_FINAL.tex`](original/P4_FINAL.tex)，逐字保留，SHA-256 为 `c38552174b2fb0dee04ed56038952437f3e3ec3bd3725a5b1ace7812703f81ed`。所有升级研究保存于 `upgrade/`，不覆盖原稿。

- [当前状态](CURRENT.md)
- [R02 停点核验、独立证明、新增原文及未核实项](upgrade/R02/VERIFICATION.md)
- [R02 有限控制化简、四控制共同达到障碍及原始研究历史](upgrade/R02/RESEARCH.md)
- [R01 原稿审查、文献、数学结果与路线判断](upgrade/R01/RESEARCH.md)
- [下一条增量核验指令](upgrade/R02/NEXT_COMMAND.md)

R01 纠正固定周期模式下确界的达到性，并给出自治紧致指定策略族的 minimax 反例及其混合反馈限制。R02 证明同控制块原子合并的精确化简，并构造四控制系统：普通不变熵为零，周期一全部 Borel 数值 minimax 两侧均为 `log 2`；指定子族有严格缺口，逐策略共同达到失败。这排除较强的证明桥梁，没有否定一般全类数值问题。

停点核验从定义复核两项 R02 证明，均通过。最新增量从 `8903b72` 恢复，补读 Huang–Ye 2009、2002a 和 2006 Toeplitz 正式全文及 Kawan 第 2 章，核清单覆盖/跨周期的量词边界与 Toeplitz 修正。2006 正文直接确认旧证错误，P4 独立计算不受影响。补齐相关索引，并给出符号合并不能自动实现共同安全控制的完整接口反例；这些没有解决一般全类数值问题。2002b 全文及 Thue–Morse 精确出处仍缺，原创性未认证。可定位证据见 VERIFICATION 第 10 节。

当前保持这条四大升级路线及整篇重写的暂停：一般数值问题未决定，没有新的通用机制或重大结构后果依据。后续只做有新材料的定向增量，不自动开 R03，不恢复增长分类，不增加路线，不降低目标，不修改其他论文或仓库。
