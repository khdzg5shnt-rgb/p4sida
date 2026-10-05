# P4：闭覆盖、采样与全部 Borel 安全反馈

仓库khdzg5shnt-rgb/p4sida。近期真实新意、独立发表及一区投稿依据，后续一区Top，长期Annals、Inventiones、JAMS、Acta。不认证或保证升级。**选刊、投稿准备及实际投稿暂停。**

- [当前结果与准确停点](CURRENT.md)
- [完整证明；第43节为固定语言的实现尝试](upgrade/R02/VERIFICATION.md)
- [下一步边界](upgrade/R02/NEXT_COMMAND.md)
- [候选TeX](upgrade/R02/P4_REVISED.tex)/[PDF](upgrade/R02/P4_REVISED.pdf)
- [R02研究](upgrade/R02/RESEARCH.md)/[R01历史](upgrade/R01/RESEARCH.md)

## 最新完整结果

从已核main 06db2ebf4191db7aa82924d73155624f12a99c0f恢复，无后续完成项。原Q=[0,6]、τ=1、四控制、安全域及完整类不变；本轮只研究全部两A Borel反馈、任意混合及原子细分，采样固定A₂。

第42节已经证明真实名字闭包的准确熵转化，并构造十位块(a,b,a,c,d,e,f,g,h,g)无限串接及十移位并Y：Y闭、σY=Y、π(Y)=Q，但h_top(P₂Y)=(4/5)log2<logρ。该抽象语言仍未实现为全域反馈。

第43节实际尝试整个Y上的字典序最小编码。它确为Borel普通截面，但其首位反馈是0在[0,4]、1在(4,6]，从60/19产生真实三周期(011)∞，违反Y全部相位；因此单步一致性失败。该反馈与贪心反射对应，偶数熵仍logρ。

随后在同一入口中完整排除全部合法阈值修复，以及它们在可数、零测或第一纲集上的修改。任意可能实现与每个阈值须有非第一纲差异，且差异测度有一个明确正下界。这是必要选控障碍，**不能推出全部Borel实现不存在，也不是数值熵改善**。

## 数值与研究裁决

没有实现成功，也没有全Borel不存在证明。任意非单调Borel选控的无限尾串一致性仍未解决。数值保持
$$
\log(3/2)\le\ell_2\le\ell_2^A\le\log\rho,
\qquad h_{A₂}(s_g)=\log\rho\approx0.55600938749,
$$
ρ⁶=ρ⁵+ρ⁴+ρ+1。本轮两上界下降量均为0，贪心最优性及两下确界精确值未决定；M₁=log2、log(3/2)≤L₁≤log2及一般问题不变。

有完整的入口失败及必要约束新证据，没有新增足够独立成篇或一区投稿依据。本次有界尝试结束并恢复暂停，不继续换语言、系统、采样或自动修补规则。

## 历史、文献与保留

VERIFICATION第1–42节全部531,404字节、R01/R02历史及九份保留文件原样不动，既有边界与暂停分支完整保留。新增精读原文0份，无新增外部定理依赖，不认证历史首创。HMY归属、Pinheiro正式版及Parry正文状态不变。2002b **未取得、未核实，获取关闭**，不索取、不循环、不替代。

候选稿 *Sparse Sampling and Borel Refinements of Closed Covers* 的TeX/PDF不改。[投稿信](upgrade/R02/COVER_LETTER_DRAFT.md)、[作者声明](upgrade/R02/AUTHOR_DECLARATIONS_DRAFT.md)、[投稿清单](upgrade/R02/SUBMISSION_CHECKLIST.md)保留，不补齐或外发。

原稿SHA-256：c38552174b2fb0dee04ed56038952437f3e3ec3bd3725a5b1ace7812703f81ed。

只更新四份记录，提交后按实际SHA全文回读十三份并核验历史、散列、父提交、树及main。只处理P4，不开R03、不恢复增长分类、不改其他项目、不改候选稿、不外发材料。
