# P4：闭覆盖、采样与全部 Borel 安全反馈

仓库khdzg5shnt-rgb/p4sida。近期真实新意、独立发表及一区投稿依据，后续一区Top，长期Annals、Inventiones、JAMS、Acta。不认证或保证升级。**选刊、投稿准备及实际投稿暂停。**

- [当前结果与阶段裁决](CURRENT.md)
- [完整证明；第41节为两A全Borel续攻及合流补步反证](upgrade/R02/VERIFICATION.md)
- [准确停点及续攻要求](upgrade/R02/NEXT_COMMAND.md)
- [候选TeX](upgrade/R02/P4_REVISED.tex)/[PDF](upgrade/R02/P4_REVISED.pdf)
- [R02研究](upgrade/R02/RESEARCH.md)/[R01历史](upgrade/R01/RESEARCH.md)

## 最新实际结果

从已核main 9f0a6e6bcbd3ad3b8a46d4a0b6bf134d2c24195e恢复，无后续完成项。原四控制系统及完整策略类保留，本轮只集中研究其全部两A合法Borel反馈、任意混合及原子细分；控制周期始终τ=1，采样A₂=(0,2,4,…)。

选择同斜率真实逆合流机制，尝试证明两A子类的贪心最优性。精确三源关系对任意Borel E成立，但中间状态选控改变合流目标位置，不能自动产生同一目标上的两步分叉。

实际反馈E_*=[3,4]在原状态的两个不变核心上分别保持贪心及其反射，全部端点与无限行程已核；其偶数熵精确为logρ。同时整个目标开区间(9/4,3)的实际两步逆像只有00分支，完整反驳了把一步合流直接延伸为偶数分叉的补步。它没有降低熵，也不反驳长路径计数或全子类最优性。

**本轮全类上界下降量为0**。最新数值仍
$$
\log(3/2)\le\ell_2\le\ell_2^A\le\log\rho,\qquad
h_{A₂}(s_g)=\log\rho\approx0.55600938749,
$$
ρ⁶=ρ⁵+ρ⁴+ρ+1。两A子类贪心最优性未证明、未反驳；ℓ₂及ℓ₂^A精确值、达到者、四控制全类贪心最优/非最优未决定。M₁=log2、log(3/2)≤L₁≤log2不变。

第41.5准确定位任意E下的真实尾部共同模式计数缺口；合流状态数不能直接替代模式数。没有数值提升或新增足够独立成篇、一区投稿依据。集中尝试结束并恢复暂停，目前没有核证的进一步计数入口。

## 历史、文献与保留

第17–40节及全部R01/R02历史原样保留，第39–40节的指定反馈反证不升级为全类下界。35.F、(28.H)/(27.R)、(29.G)、区域目标及一般问题保持原未决定范围和暂停安排。

新增精读原文0份，无新增外部依赖；新增逆关系与反馈检验自证，不认证历史首创。HMY归属、Pinheiro正式版及Parry正文状态不变。2002b **未取得、未核实，获取关闭**，不索取、不循环、不替代。

候选稿 *Sparse Sampling and Borel Refinements of Closed Covers* 的TeX/PDF不改。[投稿信](upgrade/R02/COVER_LETTER_DRAFT.md)、[作者声明](upgrade/R02/AUTHOR_DECLARATIONS_DRAFT.md)、[投稿清单](upgrade/R02/SUBMISSION_CHECKLIST.md)原样保留，不补齐或外发。

九份保留文件及VERIFICATION第1–40节原505,449字节不变。[原稿](original/P4_FINAL.tex) SHA-256：

c38552174b2fb0dee04ed56038952437f3e3ec3bd3725a5b1ace7812703f81ed

只更新四份状态/证据文件，提交后按实际SHA全文回读十三份并核验历史。只处理P4，不开R03、不恢复增长分类、不改其他项目、不改候选稿、不外发材料。
