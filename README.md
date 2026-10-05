# P4：闭覆盖、采样与全部 Borel 安全反馈

仓库khdzg5shnt-rgb/p4sida。近期真实新意、独立发表及一区投稿依据，后续一区Top，长期Annals、Inventiones、JAMS、Acta。不认证或保证升级。**选刊、投稿准备及实际投稿暂停。**

- [当前结果与阶段裁决](CURRENT.md)
- [完整证明；第42节裁决行程闭包的全覆盖下界](upgrade/R02/VERIFICATION.md)
- [准确停点及续攻边界](upgrade/R02/NEXT_COMMAND.md)
- [候选TeX](upgrade/R02/P4_REVISED.tex)/[PDF](upgrade/R02/P4_REVISED.pdf)
- [R02研究](upgrade/R02/RESEARCH.md)/[R01历史](upgrade/R01/RESEARCH.md)

## 最新实际结果

从已核main 0d1d4ad9ac061f33f5debb43f657142837d1b64f恢复，无后续完成项。原四控制系统和完整类不变，本轮只研究全部两A合法Borel反馈、任意混合及原子细分，τ=1、A₂=(0,2,4,…)不变。

对每个E，实际行程闭包Y_E非空紧致、移位包含、πβ投影满Q，并且没有新增有限偶数模式；h_top(P₂(Y_E))=h_A₂(s_E)完整成立，不需闭环连续或额外除以2。

更强的全覆盖语言logρ下界却已完整反驳。十位块(a,b,a,c,d,e,f,g,h,g)任意串接并取十个移位，得到闭集Y且σY=Y。八个投影权重的重叠不等式及无限递归证明πβ(Y)=Q；解析全部字长计数证明
$$
h_{\rm top}(P_2(Y))=\tfrac45\log2\approx0.55451774445<\log\rho.
$$
这是放宽语言类的完整反例。尚未证明Y能由一个单步一致Borel反馈实现，本轮也不转入该实现研究，因此不能将它当作ℓ₂ᴬ或原ℓ₂上界。

**本轮原全类上界下降量为0**。数值仍
$$
\log(3/2)\le\ell_2\le\ell_2^A\le\log\rho,\qquad
h_{A₂}(s_g)=\log\rho\approx0.55600938749,
$$
ρ⁶=ρ⁵+ρ⁴+ρ+1。两A子类贪心最优性、两下确界精确值及达到者未决定；M₁=log2、log(3/2)≤L₁≤log2不变。

新增转化证明与反例确实裁决一个具体命题，但没有实际反馈数值提升或新增足够独立成篇、一区投稿依据。该放宽路线结束并暂停，尚缺把同状态一致选控变成有效定量限制的步骤；不继续换语言或自动研究反馈实现。

## 历史、文献与保留

第17–41节及全部R01/R02历史原样保留。第39–41节指定反馈反证不升级为全类下界；其他暂停分支、35.F、(28.H)/(27.R)、(29.G)及一般问题保持原范围。

新增精读原文0份，无新增外部依赖。新编码、覆盖与计数证明自证，不认证历史首创；HMY归属、Pinheiro正式版及Parry正文状态不变。2002b **未取得、未核实，获取关闭**，不索取、不循环、不替代。

候选稿 *Sparse Sampling and Borel Refinements of Closed Covers* 的TeX/PDF不改。[投稿信](upgrade/R02/COVER_LETTER_DRAFT.md)、[作者声明](upgrade/R02/AUTHOR_DECLARATIONS_DRAFT.md)、[投稿清单](upgrade/R02/SUBMISSION_CHECKLIST.md)保留，不补齐或外发。

九份保留文件及VERIFICATION第1–41节原517,372字节不变。[原稿](original/P4_FINAL.tex) SHA-256：

c38552174b2fb0dee04ed56038952437f3e3ec3bd3725a5b1ace7812703f81ed

只更新四份记录，提交后按实际SHA全文回读十三份并核验历史。只处理P4，不开R03、不恢复增长分类、不改其他项目、不改候选稿、不外发材料。
