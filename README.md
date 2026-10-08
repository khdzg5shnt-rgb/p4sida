# P4：稀疏采样、逆容量与安全反馈

仓库khdzg5shnt-rgb/p4sida。**主要阅读版本为48页英文完整整合稿**，覆盖初稿主线、九页改版及截至第64节的主要完整数学成果；保留证明、非平凡例子、适用边界和未解问题。详细范围见整合说明。

- [完整论文PDF](upgrade/R02/P4_INTEGRATED.pdf) / [TeX](upgrade/R02/P4_INTEGRATED.tex)
- [整合范围与成果对应](upgrade/R02/INTEGRATION_NOTES.md)
- [当前状态](CURRENT.md)
- [完整核验及第65节整合记录](upgrade/R02/VERIFICATION.md)
- [后续安排](upgrade/R02/NEXT_COMMAND.md)
- [十篇四大论文学习](upgrade/R02/FOUR_MAJOR_STUDY.md)
- [原稿](original/P4_FINAL.tex)
- [保留九页候选TeX](upgrade/R02/P4_REVISED.tex) / [PDF](upgrade/R02/P4_REVISED.pdf)
- [R02研究](upgrade/R02/RESEARCH.md) / [R01历史](upgrade/R01/RESEARCH.md)

新稿标题为 *Sparse Sampling and Inverse Capacity in Safe Feedback Systems*。两条主要机制是：有限闭覆盖的全部Borel细化在任意预设渐疏采样上的精确值，以及真实逆列表容量指数衰减给出的全反馈最大模式阈值和精确M。有限柱系统给出源权重、跨层分散及最新增益—损失结构用途。

第64节最新结果写入第15节：原安全尾域的强制亏损配额控制全部列表历史，即使每个源端都有增益列且没有任何共同正单步非严格左预算，仍得到一类系统的全Borel反馈M₁=logq。完整列估计、任意控制数的系统族、24字母见证、安全选择器及细分范围均展开证明。不是只把研究记录附在旧九页稿后。

原稿的共同采样、符号实现、Thue–Morse及周期坍缩保留；吸收反馈、保护桥接、临界边界、实际贪心精确偶数熵及重要实现障碍一起组织。未解问题明确保留，失败模板在历史记录中，不作为贡献数量。HMY、Huang–Ye及经典矩阵工具准确归属；2002b仍“未取得、未核实，获取关闭”。

本次完整写作及核查没有新增数值定理，也不认证中科院数学大类一区、一区Top或四大。阶段目标不保证升级。作者个人信息与审阅确认没有新增事实；旧九页稿及其投稿材料保留，不自动用于新48页稿。选刊、投稿准备及实际投稿继续暂停，没有外发。

原稿、候选稿、投稿材料、R01/R02和十篇学习记录不变；仅另建整合TeX/PDF/说明，更新四份状态记录。VERIFICATION第1–64节904,400字节精确保留，追加第65节。原稿SHA-256仍为c38552174b2fb0dee04ed56038952437f3e3ec3bd3725a5b1ace7812703f81ed。按实际提交SHA全文回读七份新增/修改和十份保留文件，核验父提交、树、main和历史。只处理P4/R02，不开R03、不恢复增长分类。
