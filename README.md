# P4：闭覆盖、采样与全部 Borel 安全反馈

仓库 khdzg5shnt-rgb/p4sida。近期争取真实新意、独立发表及一区投稿依据，后续一区 Top，长期 Annals、Inventiones、JAMS、Acta。不认证或保证升级。**数学攻坚、选刊、投稿准备及实际投稿保持暂停。**

- [当前结果与准确停点](CURRENT.md)
- [十篇四大论文学习：机制、证明定位和P4适用限制](upgrade/R02/FOUR_MAJOR_STUDY.md)
- [完整核验；第43节为实现尝试，第44节为文献学习](upgrade/R02/VERIFICATION.md)
- [下一步边界](upgrade/R02/NEXT_COMMAND.md)
- [候选TeX](upgrade/R02/P4_REVISED.tex)/[PDF](upgrade/R02/P4_REVISED.pdf)
- [R02研究](upgrade/R02/RESEARCH.md)/[R01历史](upgrade/R01/RESEARCH.md)

## 最新学习记录

从已核 main 8ab86501eed9e9f27d56c6694b5182fcb209e595 开展用户授权的十篇论文学习：三篇 Annals、五篇 Inventiones、两篇 JAMS，涵盖采样独立性、符号扩张、可测编码、动力一致标记及多尺度熵。取得合法全文，核对 DOI 和版本，精读引言、主定理及指定相关证明；未宣称十篇全部证明已独立复核。

学习重点是怎样把具体的兼容性或信息损失障碍变成结构定理，并用可核证的构造跨过它。Boyle–Downarowicz、Seward、Gutman–Tsukamoto 提供了与当前实现缺口最接近的比较对象，但额外空间、零测例外及固定作用的假设不能直接用于 P4。记录区分文献结论、阅读范围、我们的判断和未完成接口，不以检索未命中认证原创性。

**本次没有新数学证明或数值改善，没有新增期刊档位认证，也没有自动启动下一轮。** 学习文件供今后的明确研究授权回查。

## 最新数学结果及未决定问题

现稿 Sparse Sampling and Borel Refinements of Closed Covers 的主线仍为第17节有限闭覆盖、全部 Borel 细化及预设渐疏采样的公式，共同后继全反馈应用和第18节完整边界保留。候选稿 TeX/PDF 不改。

第42节低熵语言 Y 为十位块 (a,b,a,c,d,e,f,g,h,g) 无限串接及十移位并。已证闭性、移位不变、满投影及 h_top(P₂Y)=(4/5)log2<logρ；辅助语言尚未由同一个无记忆 Borel 反馈实现。

第43节完整证明整个 Y 的字典序普通截面不能满足单步一致性，并排除全部阈值及可数、零测、第一纲修复。任意非单调 Borel 实现仍未决定。这些障碍不能替代全类不存在证明或数值缺口。

数值保持
$$
\log(3/2)\le\ell_2\le\ell_2^A\le\log\rho,
\qquad h_{A_2}(s_g)=\log\rho\approx0.55600938749,
$$
ρ⁶=ρ⁵+ρ⁴+ρ+1。贪心最优性及两下确界的精确值、达到者未决定；M₁=log2、log(3/2)≤L₁≤log2及一般问题不变。

## 历史、文献与保留

VERIFICATION 第1–43节原546,534字节、R01/R02历史及九份保留文件原样不动，既有边界与暂停分支保留。HMY 共同正测度熵阈值归属保留；Pinheiro 正式版及 Parry 正文状态不变。2002b **未取得、未核实，获取关闭**，不索取、不循环、不替代。

[投稿信](upgrade/R02/COVER_LETTER_DRAFT.md)、[作者声明](upgrade/R02/AUTHOR_DECLARATIONS_DRAFT.md)、[投稿清单](upgrade/R02/SUBMISSION_CHECKLIST.md)保留，不补齐或外发。原稿 SHA-256：c38552174b2fb0dee04ed56038952437f3e3ec3bd3725a5b1ace7812703f81ed。

本次只新增学习文件并更新四份记录，提交后按实际 SHA 全文回读十四份新增/更新与保留文件，核验历史前缀和散列。只处理 P4，不开 R03、不恢复增长分类、不改其他项目、不改候选稿、不外发材料。
