# P4：闭覆盖、采样与全部 Borel 安全反馈

仓库khdzg5shnt-rgb/p4sida。近期争取真实新意、独立发表，后续一区/Top，长期Annals、Inventiones、JAMS、Acta。不认证或保证升级。**选刊、投稿准备及实际投稿暂停。**

- [当前成果与阶段裁决](CURRENT.md)
- [完整证明；第39节为贪心精确熵及短复位障碍](upgrade/R02/VERIFICATION.md)
- [准确停点及续攻要求](upgrade/R02/NEXT_COMMAND.md)
- [候选TeX](upgrade/R02/P4_REVISED.tex)/[PDF](upgrade/R02/P4_REVISED.pdf)
- [R02研究](upgrade/R02/RESEARCH.md)/[R01历史](upgrade/R01/RESEARCH.md)

## 最新完整结果及数值范围

从已核main f2a855a495f4c527bfc84283fc73ebb1751b6759恢复，无后续完成项。原四仿射系统、Q=[0,6]、τ=1、全部合法Borel反馈、任意混合及原子细分不变，采样仅A₂=(0,2,4,…)。

实际攻击B1短复位反馈：在[12/5,241/100)选B1，其余沿用s_g。新规则全域一致安全，核心轨道确被改变。完整实际逆路径却证明：对任意Borel E⊂[12/5,162/65)，在E选B1、其余贪心的模板，全部没有相邻1100块的0/10/1100完整块串仍能实现。每个奇数控制、中间状态及有限串之后的无限行程都被核对；不是辅助语言自动实现。计数及真实次乘给
$$
N_k(s_E)\ge\rho^k\ (\forall k\ge1),\qquad h_{A₂}(s_E)\ge\log\rho.
$$
因此该复位模板在任何字长都不能严格降低logρ上界；不排除其他合法反馈。取E=∅并调用第38节上界，新增
$$
\boxed{h_{A₂}(s_g)=\log\rho\approx0.55600938749,\qquad
\rho^6=\rho^5+\rho^4+\rho+1.}
$$
贪心偶数熵已确定；完整类贪心最优或非最优仍未决定。未来任何真实反馈严格上界c<logρ均足以证明非最优，不再必须先越过logφ。

**本轮全类上界下降量为0**，仍log(3/2)≤ℓ₂≤logρ，ℓ₂精确值及达到者未决定；L₁区间仍log(3/2)≤L₁≤log2，M₁=log2。固定采样单反馈精确值和指定族反证不能决定全部采样的minimax。

有完整、有限的数学增量，没有新增足够依据确认独立成篇或一区投稿。所选尝试结束并恢复暂停；还缺全域一致的新规则及其全部模式严格上界，不继续只换复位带、增加字长或列条件命题。

## 历史、文献与保留

第17节闭覆盖与共同后继、第18节边界及第23–38节全部历史保留。第35节密度一采样精确值、第36节s_per、第37节次乘与优化准确范围直接采用。35.F、(28.H)/(27.R)、(29.G)、区域目标及一般问题保持原未决定范围和暂停安排。

新增精读原文0份，无新增外部依赖；新路径论证自证，不认证历史首创。HMY归属、Pinheiro正式版及未读Parry正文状态不变。2002b **未取得、未核实，获取关闭**，不索取、不循环、不替代。

候选稿 *Sparse Sampling and Borel Refinements of Closed Covers* 的TeX/PDF不改。[投稿信](upgrade/R02/COVER_LETTER_DRAFT.md)、[作者声明](upgrade/R02/AUTHOR_DECLARATIONS_DRAFT.md)、[投稿清单](upgrade/R02/SUBMISSION_CHECKLIST.md)原样保留，不补齐或外发。

九份保留文件及VERIFICATION第1–38节原479,159字节不变。[唯一原稿](original/P4_FINAL.tex) SHA-256：

c38552174b2fb0dee04ed56038952437f3e3ec3bd3725a5b1ace7812703f81ed

只更新四份状态/证据文件，提交后按实际SHA全文回读十三份并核验历史。只处理P4，不开R03、不恢复增长分类、不改其他项目、不自动改写候选稿、不外发材料。
