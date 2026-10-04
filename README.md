# P4：闭覆盖、采样与全部 Borel 安全反馈

仓库 khdzg5shnt-rgb/p4sida。分阶段目标：近期有实质新意、独立成篇及一区投稿依据，后续一区 Top，长期 Annals、Inventiones、JAMS、Acta。不是档位认证或升级保证。**选刊、投稿准备与实际投稿暂停。**

- [当前成果与阶段裁决](CURRENT.md)
- [完整证据；第 25 节为最新有界续攻](upgrade/R02/VERIFICATION.md)
- [唯一数值缺口及后续指令](upgrade/R02/NEXT_COMMAND.md)
- [九页候选 TeX](upgrade/R02/P4_REVISED.tex) / [PDF](upgrade/R02/P4_REVISED.pdf)
- [R02 研究](upgrade/R02/RESEARCH.md) / [R01 历史](upgrade/R01/RESEARCH.md)

## 最新结果与限制

从 67109998bbffcb2b5b1d79de484c2331a4f91bff 恢复。第 25 节只攻击一个无整数分支的双扩张核心：Q=[0,R]，四控制 ax、ax−(a−1)R、bx、bx−(b−1)R，1<a,b<2，log a/log b 无理，周期固定为 1，全 Borel 反馈及混合/细分保留。

**完整否定结果：** 类型交替的辅助图语言即使补入全部有限交替前缀与端点常值尾，也不能实现为全域 Borel 安全反馈。逆分支覆盖整个状态约束、图语言模式指数为 log 2，仍不足以实现单步一致选码。真实端点附近行程在对数尺度上迫使无理旋转的可测二着色，矛盾；完整证明见 25.2–25.4。

具体例 a=3/2、b=5/3、Q=[0,6] 无非空整数斜率仿射复合。基础覆盖、两标签反馈和已知量化给 **M₁=log 2、log(3/2)≤L₁≤log 2**。这些不是主要新增贡献。实现反例不决定 L₁，不给一般 L<M，也不排除其他反馈达到 M₁。

**数值区间未缩小，仍没有新增的合理一区投稿依据。** 已知二着色障碍的原文、版本、勘误和 DOI 已定向核对；双尺度归约是仓库新增推导，历史首创未认证。停止本项，不换语言或系统接着试。唯一数值缺口是将非整数容量证书提升为预先固定、对全部反馈有效的 log 2 采样阈值，目前没有已验证入口。

## 可靠成果与历史

第 23 节整数吸收反馈及窗口计数、第 24 节全局扩张分支扩充的全类精确值、所有固定周期的连续共同因子排除和折叠反例完整保留，未重复计算。

候选稿 *Sparse Sampling and Borel Refinements of Closed Covers* 仍为九页，TeX/PDF 未改。第 17 节有限闭覆盖、任意预设渐疏采样的全 Borel 细化公式及共同后继应用、第 18 节适用边界不变。HMY 已有共同正测度阈值归属保留；第 20 节专门短文成篇理由不是一区升级认证。

[投稿信](upgrade/R02/COVER_LETTER_DRAFT.md)、[作者声明](upgrade/R02/AUTHOR_DECLARATIONS_DRAFT.md)、[投稿清单](upgrade/R02/SUBMISSION_CHECKLIST.md) 原样保存，不补齐或外发。

一般 minimax 未决定，√2、Ω、m₂、第 19 节旧接口暂停，2002b **未取得、未核实，获取关闭**。原稿、R01/R02 历史和 VERIFICATION 第 1–24 节（260,353 字节）完整保留。

[唯一原稿](original/P4_FINAL.tex) SHA-256：

c38552174b2fb0dee04ed56038952437f3e3ec3bd3725a5b1ace7812703f81ed

本轮四份状态/证据文件更新，按实际 SHA 全文回读十三份并核验保留内容。只处理 P4，不开 R03、不恢复增长分类、不改其他项目。
