# P4 当前状态：全文核验及JDE对照后的56页英文结构审阅稿

更新：2026-10-10（北京时间）。本轮从main `32aebfe608aeb818c8ab1eb46360d60d8dca0846`、树 `fdbc1bac5a1939b548ad1a701c5331bc63675cc6`恢复；中断恢复后未发现后续提交，适用祖先目录及完整仓库树未发现AGENTS.md。用户明确授权的完整数学核验、五篇JDE全文对照和实际英文结构整理已落实。

## 现行版本

- [56页现行PDF](upgrade/R02/P4_STYLE_REVIEWED.pdf) / [TeX](upgrade/R02/P4_STYLE_REVIEWED.tex)
- [全文数学核验、五篇原文对照和内容去向](upgrade/R02/P4_MATH_STYLE_REVIEW.md)
- [保留的60页选择补回稿](upgrade/R02/P4_SELECTED_REVIEWED.pdf) / [TeX](upgrade/R02/P4_SELECTED_REVIEWED.tex) / [当时取舍报告](upgrade/R02/CONTENT_SELECTION_REVIEW.md)
- [保留的54页补全稿](upgrade/R02/P4_COMPLETE_REVIEWED.pdf) / [TeX](upgrade/R02/P4_COMPLETE_REVIEWED.tex)

本轮独立检查60页稿所有定义、假设、43项定理类结果、6个编号例子、全部证明与未编号推导，以及结构修订影响的声明。没有发现需要改变主定理、假设或数值的实质数学错误；没有识别出最终保留已证声明的未修复缺口。这不是形式化证明、作者确认或同行审定。历史标签只用于定位。

正文18节合并为11节，摘要、引言、段落引导及结尾实际重写。一项纯组合反例移至G.1；强迫前驱核层及嵌套可行链两组辅助工具完整留在60页稿及研究记录。周期种子反例依赖的相位判据保留在C.2前，并修复移动造成的回指。上轮六组内容按具体结论重新选择，非全部删去或全部强留。现稿42项定理类结果和6个例子，43个保留proof环境逐字不变，47个编号环境逐字不变，另1个仅改相位回指。

五篇JDE文章已核实正式发表且完整阅读：Nie–Wang–Huang、Colonius–Cossich–Santana、Ayala等、Ban等、Shao。两篇出版版、三篇作者公开全文；后三篇未逐字核对最终出版版，Shao所读为2023年v1，正式卷年2026。报告给出DOI、原文链接、版本、阅读位置和具体修改，不声称达到JDE发表标准，不提供AI检测率。论文12项文献及AI说明与60页稿逐字相同。

实际编译56页，197标签唯一，原稿70标签保留，全部引用、交叉引用和编号按最终aux核对；全部页面渲染并视觉检查，无编译错误/警告、Overfull或Underfull。页面减少来自结构取舍，未按目标页数删改。

## 数值与停点

原Q=[0,6]保持M₁=log2、log(3/2)≤L₁≤log2、log(3/2)≤ℓ₂≤ℓ₂ᴬ≤logρ、h_A₂(s_g)=logρ及ρ⁶=ρ⁵+ρ⁴+ρ+1。循环例保持M₁=log2及log(q/(q−1))≤L₁≤log2，未断言L=M。其他原精确值不变。

一般共同采样、原系统精确L₁/偶数优化及贪心最优性、√2/Ω任意实现、Y/H满覆盖及一致Borel实现、一般满支撑标量化、全反馈返回抽取、无限可行链和其他暂停分支仍未解决且未重开。2002b保持“未取得、未核实，获取关闭”。只处理P4/R02，不分派代理，不开R03、不恢复增长分类、不选刊、不投稿、不联系他人。

## 保留及提交核验

另建STYLE TeX/PDF和P4_MATH_STYLE_REVIEW；更新本文件、README、NEXT_COMMAND，VERIFICATION仅追加第70节。其余24份基线文件字节及Git blob保持，包括全部旧稿和研究记录。原稿SHA-256仍为`c38552174b2fb0dee04ed56038952437f3e3ec3bd3725a5b1ace7812703f81ed`；VERIFICATION原938,458字节前缀SHA-256仍为`ce3a858ff159b4c9ffe8241a36d90289a9ce7ca8cb6915d0aa4fce89857606e8`。

提交使用已核main、实际base tree及expected_sha lease；提交后按实际SHA全文回读7份新增/修改与24份保留文件，核验父提交、树、main和历史前缀。实际最终SHA随交付提供，不预填未来SHA。恢复及停点见[NEXT_COMMAND](upgrade/R02/NEXT_COMMAND.md)。
