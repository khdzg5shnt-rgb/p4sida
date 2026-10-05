# P4：闭覆盖、采样与全部 Borel 安全反馈

仓库khdzg5shnt-rgb/p4sida。近期真实新意、独立发表及一区投稿依据，后续一区Top，长期Annals、Inventiones、JAMS、Acta。不认证或保证升级。**选刊、投稿准备及实际投稿暂停。**

- [当前结果与阶段裁决](CURRENT.md)
- [完整证明；第40节为高位B1的全字长构造反证](upgrade/R02/VERIFICATION.md)
- [准确停点及续攻要求](upgrade/R02/NEXT_COMMAND.md)
- [候选TeX](upgrade/R02/P4_REVISED.tex)/[PDF](upgrade/R02/P4_REVISED.pdf)
- [R02研究](upgrade/R02/RESEARCH.md)/[R01历史](upgrade/R01/RESEARCH.md)

## 最新实际结果

从已核main 0464eccba97d8d361653f9dde5896dddf96d2907恢复，无后续完成项。原Q=[0,6]、τ=1、四仿射控制及完整策略类不变；采样仅A₂=(0,2,4,…)。

选择高位B1核心规则：在[26/9,3)选B1，其余沿用贪心。它全域Borel、安全、同状态一致，确实破坏旧1100实际字典。但完整的原周期一两步像核对证明，新码0、10、B0000、B010010、B0B0000都能真实返程到整个核心，并可自由串接。偶数B1标签完整计数，奇数B1中间分支也保留。解析码数及已核次乘给
$$
h_{A₂}(s_H)\ge\log\lambda\approx0.55888371598>\log\rho,
\qquad N_k(s_H)\ge\lambda^k>\rho^k\quad(\forall k\ge1),
$$
其中λ⁷=λ⁶+λ⁵+λ²+2。这个固定规则已完整证明劣于贪心，不能在任何字长实现严格改善；不是有限搜索外推，也不排除其他反馈。

**本轮全类上界下降量为0**。最新数值仍为
$$
h_{A₂}(s_g)=\log\rho\approx0.55600938749,\qquad
\log(3/2)\le\ell_2\le\log\rho,
$$
ρ⁶=ρ⁵+ρ⁴+ρ+1。ℓ₂精确值、达到者及贪心全类最优/非最优未决定；M₁=log2、log(3/2)≤L₁≤log2不变。固定采样具体构造反证不能决定全部采样数值问题。

新增完整反证揭示了实际标签替换后的模式成本，没有数值提升或新增足够独立成篇、一区投稿依据。集中尝试结束并恢复暂停；还缺全域一致规则及全部真实模式严格上界，目前没有核证入口。

## 历史、文献与保留

第17节闭覆盖与共同后继、第18节边界及第23–39节全部历史原样保留。第35–37节准确范围及第39节贪心精确值、短复位模板反证直接采用。35.F、(28.H)/(27.R)、(29.G)、区域目标及一般问题保持原未决定范围和暂停安排。

新增精读原文0份，无新增外部依赖；第40节自证，不认证历史首创。HMY归属、Pinheiro正式版及未读Parry正文状态不变。2002b **未取得、未核实，获取关闭**，不索取、不循环、不替代。

候选稿 *Sparse Sampling and Borel Refinements of Closed Covers* 的TeX/PDF不改。[投稿信](upgrade/R02/COVER_LETTER_DRAFT.md)、[作者声明](upgrade/R02/AUTHOR_DECLARATIONS_DRAFT.md)、[投稿清单](upgrade/R02/SUBMISSION_CHECKLIST.md)原样保留，不补齐或外发。

九份保留文件及VERIFICATION第1–39节原492,597字节不变。[原稿](original/P4_FINAL.tex) SHA-256：

c38552174b2fb0dee04ed56038952437f3e3ec3bd3725a5b1ace7812703f81ed

只更新四份状态/证据文件，提交后按实际SHA全文回读十三份并核验历史。只处理P4，不开R03、不恢复增长分类、不改其他项目、不自动改写候选稿、不外发材料。
