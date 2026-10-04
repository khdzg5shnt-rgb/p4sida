# P4：闭覆盖、采样与全部 Borel 安全反馈

仓库khdzg5shnt-rgb/p4sida。近期争取实质新意、独立成篇及一区投稿依据，后续一区Top，长期Annals、Inventiones、JAMS、Acta。不是档位认证或升级保证。**选刊、投稿准备及实际投稿暂停。**

- [当前成果与阶段裁决](CURRENT.md)
- [完整证据；第33节为最新集中尝试](upgrade/R02/VERIFICATION.md)
- [停点与续攻条件](upgrade/R02/NEXT_COMMAND.md)
- [候选TeX](upgrade/R02/P4_REVISED.tex)/[PDF](upgrade/R02/P4_REVISED.pdf)
- [R02研究](upgrade/R02/RESEARCH.md)/[R01历史](upgrade/R01/RESEARCH.md)

## 最新结果

从dced2ee55fa3731421ae695d4b4be49c7ff9a0db恢复并核对main，无后续成果。保持原Q=[0,6]四仿射控制、τ=1、全部合法Borel反馈、任意混合及原子细分。

第33节选择无限逆树S={0}∪{2(2/3)^n(3/5)^m:n,m≥0}，完整核验其紧致性、一步可行及无记忆反馈实现。其逐层缩小的闭邻域确有内部、分量尺度趋零；但取全部迭代后的核，内部仍全部消失。

决定性完整证明：**任何闭可行区域K⊂[0,2+1/100]都为Lebesgue零测度。** 在这个原安全范围内，实际首返只有两种可交换零分支及A1；按使用次数归并后，小返回区间[0,3/200]到自身的总逆容量小于3/16。因此所选无限逆树的每层核都包含无限S，却没有开区间。这超出第32节有限极限排除，但没有构造成功链。

**无限嵌套闭可行链仍未决定。** 其他位置及两种平移均参与的回返结构没有被排除；仍缺完整无限期内部存续及分量尺度控制。

**(29.G)、(28.H)与L₁无新决定；M₁=log2，log(3/2)≤L₁≤log2。** 本轮是构造边界，有界尝试结束并恢复暂停，尚无新增独立成篇或一区升级依据。不把状态逆像的测度容量当作控制名字的模式计数。

## 历史与保留

第17节闭覆盖与共同后继结果、第18节完整边界、第23–32节已证成果和失败范围完整保留，不将局部排除写成一般不可能。

候选稿 *Sparse Sampling and Borel Refinements of Closed Covers* 的TeX/PDF不改。[投稿信](upgrade/R02/COVER_LETTER_DRAFT.md)、[作者声明](upgrade/R02/AUTHOR_DECLARATIONS_DRAFT.md)、[投稿清单](upgrade/R02/SUBMISSION_CHECKLIST.md)原样保存，不补齐或外发。

新增精读原文0份，无新增外部定理依赖；完整首返容量证明见33.3。历史最早覆盖及Pinheiro正式期刊版未核实，HMY归属不变，不认证原创性或期刊档位。

一般minimax未决定；√2、Ω、m₂、第19节旧接口暂停；2002b **未取得、未核实，获取关闭**。九份保留文件及VERIFICATION第1–32节原391,937字节不变。

[唯一原稿](original/P4_FINAL.tex) SHA-256：

c38552174b2fb0dee04ed56038952437f3e3ec3bd3725a5b1ace7812703f81ed

仅更新四份状态/证据文件，提交后按实际SHA全文回读十三份并核验历史。只处理P4，不开R03、不恢复增长分类、不改其他项目、不自动改写候选稿、不外发材料。
