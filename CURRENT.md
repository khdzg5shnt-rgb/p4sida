# P4当前状态：全文数学复核后的43页英文稿

2026-10-09 UTC。基线main为`2d59ebfc1db0bad0c6697a82b980affd5b967390`，树为`77792c00a864bf1a5307f46ba80e842bc8ca74ab`。

- [现行PDF](upgrade/R02/P4_FINAL_CHECKED.pdf) / [TeX](upgrade/R02/P4_FINAL_CHECKED.tex)
- [全文数学与阅读修订报告](upgrade/R02/FINAL_MATH_READABILITY_CHECK.md)
- [保留的42页DCDS稿](upgrade/R02/P4_DCDS_REVIEWED.pdf) / [TeX](upgrade/R02/P4_DCDS_REVIEWED.tex) / [十篇原文对照及取舍](upgrade/R02/DCDS_COMPARATIVE_REVIEW.md)
- [52页稿](upgrade/R02/P4_REWRITTEN.pdf) / [57页稿](upgrade/R02/P4_FINAL_REVIEWED.pdf) / [56页稿](upgrade/R02/P4_STYLE_REVIEWED.pdf) / [60页稿](upgrade/R02/P4_SELECTED_REVIEWED.pdf) / [54页稿](upgrade/R02/P4_COMPLETE_REVIEWED.pdf)

## 本轮完成

连续阅读完整正文及附录，独立复核34个编号结果、31个正式证明、未编号计算及依赖。核对真实反馈、全域安全、Borel性、无限延续、量词、端点、原子细分、实际支撑计数、固定/可选采样和子类/全类。回查Kerr–Li、Huang–Ye及Kawan实际使用的一手证明，不沿用旧“已证”标签。

未发现需要改变定理、假设或数值的错误。修正Kawan Definition 2.8的“不变覆盖/分割”归属；区分算子段的密度与质量；展开源列权重选择、贪心逆路径拼接、稀疏族两层并集估计，减少重复强调和空泛过渡。全部结果及附录分工保留，无新增、移动或删除。原十篇DCDS全文及比较成果沿用，没有重复研究。

有理数复算矩阵三因子25/27、源列系数13/15、保护区间端点及贪心逆路径62项分段检查；这些只核有限证书，无限时间结论仍由证明给出。编译并查看全部43页，157标签编号与前版一致，34编号结果、31个proof、11文献不变，无编译/版式警告。AI说明与参考文献逐字保持。

## 结论与停点

本轮未发现尚待修复的具体证明缺口，但不是形式化验证或外部审稿。四分支仍M₁=log2、log(3/2)≤L₁≤log2、log(3/2)≤ℓ₂≤ℓ₂ᴬ≤logρ，贪心偶采样率仍logρ。一般共同采样、精确L₁与偶采样最优性、贪心最优性及既往暂停问题未解决、未续攻。

C/D/F的选择和转折已增加解释，技术推导仍需专业阅读。没有独立读者认可证据，不宣称AI感消失、胜过参照文章或获得发表保证；不再机械换词。2002b仍“未取得、未核实，获取关闭”。

## 保存

新增3份、更新4份，其余36份基线文件保留。VERIFICATION只追加§74，前962103字节SHA-256为`4afaa51c447f3acb99b803473b0257810b7924f8a920efe3cc0a3692dd3b2a18`；原稿SHA-256为`c38552174b2fb0dee04ed56038952437f3e3ec3bd3725a5b1ace7812703f81ed`。提交前核main，以expected_sha非强制更新；提交后按实际SHA全文回读43份并核父提交、树、main和历史字节，实际结果随交付给出。仅P4/R02，无代理、P3/P6读改、新研究、R03、增长分类、投稿或对外联系。
