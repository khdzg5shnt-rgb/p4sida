# P4：闭覆盖、采样与全部 Borel 安全反馈

这是 khdzg5shnt-rgb/p4sida 的 P4 研究仓库。当前分阶段扩展：近期争取有实质新意和一区投稿依据的主定理，后续争取一区 Top，长期争取 Annals、Inventiones、JAMS、Acta。阶段是目标，不是已达档位或必然升级链。**投稿准备和实际投稿暂停。**

- [当前成果及阶段裁决](CURRENT.md)
- [核验证据；第 23 节为最新数学扩展](upgrade/R02/VERIFICATION.md)
- [下一步的具体缺口与边界](upgrade/R02/NEXT_COMMAND.md)
- [九页候选 TeX](upgrade/R02/P4_REVISED.tex) / [PDF](upgrade/R02/P4_REVISED.pdf)
- [R02 原始研究](upgrade/R02/RESEARCH.md) / [R01 历史](upgrade/R01/RESEARCH.md)

## 最新数学进展与限度

从 454266d05e9f5f2901d8b13533b8556a5df55256 恢复后，本轮证明自然整数仿射族的全类精确值：整数 m≥2、D≥m，Q=[0,D/(m−1)]、U={0,…,D}、安全转移 mx−u。**每个固定周期 τ 的全部合法 Borel 安全选择器、任意混合及细分均有 Lτ=Mτ=log m。** 完整反馈、全部状态安全、实际块行程、任意窗口计数与全类下界见第 23 节。

机制是进入整数编码核心前只有一个单向过渡段；吸收时间无统一上界，任意窗口仍只增加多项式数量模式。例 m=D=3、τ=1 的最少安全覆盖数为 4，而全类值为 log 3；反馈改变后继，覆盖公式失效，一般 L=M 未被反驳。

**系统范围有实际增量，尚不构成一区升级主贡献。** 分支仍共享模 1 扩张因子，核心为标准整数满移位，体积和有限阶段计数为基础工具。原文对照、独立新意及成篇判断见 23.8–23.9。未用检索未命中认证原创性，未借已发表论文所在刊给本结果升档。

下一步缺的是核心商动力学也随反馈变化时的全类共同下界，以及与真实吸收反馈模式上界的匹配机制。目前无已验证入口，本轮停止，不自动换系统或重开旧接口。

## 现有候选稿与历史

*Sparse Sampling and Borel Refinements of Closed Covers* 仍为九页，TeX/PDF 未改。主线为任意预设渐疏采样下，混合有限型移位幂有限闭覆盖的全 Borel 细化精确值 log N(K)，共同后继应用为 log r/τ；第 18 节完整边界保留。承认 HMY 已有共同正测度阈值。第 20 节专门短文成篇理由保留，不等于一区升级依据。

[投稿信](upgrade/R02/COVER_LETTER_DRAFT.md)、[作者声明](upgrade/R02/AUTHOR_DECLARATIONS_DRAFT.md)、[投稿清单](upgrade/R02/SUBMISSION_CHECKLIST.md) 原样作为历史草稿保存，当前不补齐、不适配、不发送。

一般全 Borel minimax 未决定；√2、Ω、m₂、第 19 节旧接口继续暂停。2002b **未取得、未核实，获取关闭**，不索取、不循环、不替代。原稿、R01/R02 历史及 VERIFICATION 第 1–22 节保留。

唯一原稿 [original/P4_FINAL.tex](original/P4_FINAL.tex) SHA-256：

c38552174b2fb0dee04ed56038952437f3e3ec3bd3725a5b1ace7812703f81ed

本轮四份状态/证据文件更新，按实际 SHA 全量回读十三份文件并核验保留内容。只处理 P4，不开 R03、不恢复增长分类、不改其他项目。
