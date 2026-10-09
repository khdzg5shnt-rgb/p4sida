# P4：DCDS原文对照、内容取舍与英文修订

2026-10-09 UTC。基线main：`70d6488e0cc7a91fc20e274aedd3733ea0a82b7b`；树：`514ad01316a7237971abc7be63fb0734399df1e4`。现行交付为[P4_DCDS_REVIEWED.tex](P4_DCDS_REVIEWED.tex)及[42页PDF](P4_DCDS_REVIEWED.pdf)。52页[P4_REWRITTEN](P4_REWRITTEN.tex)及所有更早稿保留；下文“旧”均指52页稿。页数是实际取舍后的结果，不是目标。

## 1. 阅读范围和判断标准

完整读取CURRENT、README、NEXT_COMMAND、READABILITY_REWRITE、52页TeX及全部PDF页面；依据实际依赖回查原稿和旧记录。37份基线文件按实际提交的字节、Git blob及SHA-256核对，未发现后续完成项或适用AGENTS.md。导师关于难读、AI式表达的反馈作为重新检查的起点，不采用旧“合格”判断。

在读参照和修订前固定七个维度：问题及贡献关系；定义引入顺序；主结果/已知工具/推论的区分；证明选择和转折；例子的任务；正文和附录的联系；密度、重复与流程口吻。比较对象是专业读者的理解负担，不是AI检测，也不是发表结果的倒推。

实际障碍有四类：§§2、3、5、6反复启动相近的计数框架；产品算子出现时尚不清楚它控制哪个集合；并列辅助准则和独立反例分散核心问题；有些范围提醒反复插入而未就地说明数学原因。本轮实质修改这些位置，未对已清楚的证明机械换词。

## 2. 十篇核实书目、全文版本与逐篇对照

以下均已核实为**Discrete and Continuous Dynamical Systems主刊（DCDS-A）原创研究论文**，不是B/S系列。逐篇读完正文、所有证明、存在的附录及参考文献，共272个PDF页；其中2篇出版版、8篇作者稿。作者稿版本号和比较页码明确列出，不把其措辞、编号或页数冒充出版版。正式书目信息依出版社DOI页面核实，全文比较依指定PDF。Da Silva–Kawan（2016）略超近十年窗口，因与控制不变性熵及两类界的组织直接相关而保留；其余九篇发表于2017–2026。没有缺额。此阅读不是对十篇论文逐条数学正确性的独立审计，也没有将其中疑似笔误移入P4。

**1. Colonius, F. (2018).** Invariance entropy, quasi-stationary measures and control sets. *Discrete and Continuous Dynamical Systems, 38*(4), 2093–2123. https://doi.org/10.3934/dcds.2018086

[出版记录](https://www.aimsciences.org/article/doi/10.3934/dcds.2018086)；[全文作者稿](https://arxiv.org/pdf/1705.08658v2)，v2，31页全部阅读（arXiv版本日期2017-11-27，稿内日期2018-10-11）。§1 pp.1–2先区分控制信息的极小化和动力熵的极大化；§2 pp.3–8按用途引入量；§2.15–2.16 pp.11–12明确归属Kawan公式；§4 pp.16–22先作局部化，§5 pp.23–30再给控制集条件；例2.17、5.12、5.13重复利用同一系统；p.30以一个具体剩余问题结束，无附录。对应P4引言、§5.2、§6.2及§8：合并名字定义，明确已知公式和直接后果，结尾只围绕共同采样。**比较**：问题呈现现已相近地先交代优化对象；P4阅读负担仍更重，需同时处理两种优化及真实支撑；证明解释在框架衔接处改善，但尚无独立试读证据；贡献定位不可直接排高低，该文的条件概率/几乎处处安全与P4全状态计数不同。该文九条早期remarks本身也密集，未照搬其组织。

**2. Qiao, Y., & Zhou, X. (2017).** Zero sequence entropy and entropy dimension. *Discrete and Continuous Dynamical Systems, 37*(1), 435–448. https://doi.org/10.3934/dcds.2017018

[出版记录](https://www.aimsciences.org/article/doi/10.3934/dcds.2017018)；[出版版全文](https://pdfs.semanticscholar.org/2367/354fd4e5c8842a13df9f846c5553fe72317a.pdf)，14页全部阅读。pp.435–437迅速给出两个目标；pp.439–441先解释熵维数所补的信息；pp.442–444将证明分为有限线性模型、分离、指数下界三个有因果关系的任务。无附录或独立结语。P4 §4.2–4.4新增两步算子展开及“纤维质量→列表覆盖→独立坐标”的理由；§6.1从同一覆盖数说明经典比较。**比较**：P4问题已可定位，但不如该文两目标紧凑；符号和技术负担仍较大；容量证明的步骤解释已更接近这种功能性安排；该文研究诱导概率测度空间的动力学，贡献不能与反馈优化直接排名。

**3. Da Silva, A., & Kawan, C. (2016).** Invariance entropy of hyperbolic control sets. *Discrete and Continuous Dynamical Systems, 36*(1), 97–136. https://doi.org/10.3934/dcds.2016.36.97

[出版记录](https://www.aimsciences.org/article/doi/10.3934/dcds.2016.36.97)；[全文作者稿](https://arxiv.org/pdf/1408.2416v1)，v1，45页全部阅读（arXiv 2014-08-11，稿内2018-07-18）。§1 pp.1–2区分上界、下界及相等；§3.1 p.7在技术前解释为何需要正则周期近似；§3.3 pp.10–16逐层去掉假设；§4.1 pp.18–30的长体积引理有九个互相依赖步骤；§4.8 pp.32–35把体积接到熵并处理极限；§5 pp.35–44合并条件与界。无附录。P4摘要/引言明确共同后继路线给L=M，而一般容量路线给M；附录D完整保留，不能因长而截掉逆路径实现。**比较**：两条路线的关系现已交代，但P4没有该文匹配上下界的统一结局；不能靠文字制造这种贡献强度。两稿都有实质技术负担；P4并非因更短就更易读，D仍需仔细计算。借鉴的是证明任务的衔接，非匹配界的叙事结论。

**4. Pavlov, R., & Vanier, P. (2021).** The relationship between word complexity and computational complexity in subshifts. *Discrete and Continuous Dynamical Systems, 41*(4), 1627–1648. https://doi.org/10.3934/dcds.2020334

[出版记录](https://www.aimsciences.org/article/doi/10.3934/dcds.2020334)；[全文作者稿](https://arxiv.org/pdf/1903.04325v1)，2019-03-11，22页全部阅读。§1 pp.1–3虽列很多结果，但按必要性和实现分组；§3.1 p.8明确两组引理分别控制什么，pp.9–11落实；§4 pp.12–21复用构造部件；§5 pp.21–22反例标出实现类边界，无附录/单列结语。P4 §5.6降为直接推论；附录F保留点态共同达到的反例，但先讲它与共同极小值的区别。**比较**：P4不再把直接推论列成等量贡献，定位较原稿清楚；两稿结果罗列都可能增加负担，不能按数量评优；F的构造目的已补，但细节仍难；计算复杂度谱与安全反馈的数学贡献不可比。本轮没有恢复增长分类研究。

**5. Lin, Z., & Ouyang, K. (2025).** Subshifts on open proximal extensions. *Discrete and Continuous Dynamical Systems, 45*(8), 2566–2590. https://doi.org/10.3934/dcds.2024176

[出版记录及出版版全文](https://www.aimsciences.org/article/doi/10.3934/dcds.2024176)；[PDF](https://www.aimsciences.org/data/article/export-pdf?id=676bcb516d9f3b103d7ed508)，25页全部阅读。§1.1 pp.2567–2568先说marker/basic words分工及开放性的困难；§2.5 p.2570说明两个置换的用途；§3.2 pp.2579–2583多种边界情形是证明所需；§4 pp.2584–2588让同一构造承担熵结论；§5 p.2589留下一个问题，无附录。P4 §4先解释列表和乘积，F.2先说稀疏族需要两个性质，§8聚焦一个未解环节。**比较**：P4局部定义目的现在更清楚，但全篇仍不如此文围绕单一构造集中；长证明均不能只凭长度删；P4的反例功能已标出，贡献关系仍比该文分散。其后续更强结论也包含早期估计，并非所有教学性重复都应删除。

**6. Zimmermann, E. (2022).** Fiber entropy and algorithmic complexity of random orbits. *Discrete and Continuous Dynamical Systems, 42*(11), 5289–5308. https://doi.org/10.3934/dcds.2022098

[出版记录](https://www.aimsciences.org/article/doi/10.3934/dcds.2022098)；[全文作者稿](https://arxiv.org/pdf/2108.13019v4)，2022-08-30，20页全部阅读。§1 pp.1–3由Brudno定理提出扩展；§3.3 pp.10–12用零/无限纤维熵例区分结论；§4 pp.13–14先约化符号问题，pp.15–17解释S遍历不能直接推出S^k遍历，随后给剩余类平均；p.18再导出分解结论。无附录/独立结语。P4 §4在定义处解释全局列表不同于逐点选择，§5.2在闭包处解释有限见证不同于单一无限见证，§5.6用推论表达。**比较**：这些局部限制的说明现已接近该文的就地解释；P4整体仍需处理更多对象，未证明更易读；其a.e.轨道复杂度不能代替P4实际支撑计数，贡献不可数值排名。

**7. Šotola, J. (2018).** Relationship between Li-Yorke chaos and positive topological sequence entropy in nonautonomous dynamical systems. *Discrete and Continuous Dynamical Systems, 38*(10), 5119–5128. https://doi.org/10.3934/dcds.2018225

[出版记录](https://www.aimsciences.org/article/doi/10.3934/dcds.2018225)；[全文作者稿](https://arxiv.org/pdf/1801.00139v1)，2017-12-30，10页全部阅读，另查看pp.5、7图。§§1–2 pp.1–3由自治情形的关系引入非自治失败；§3 pp.4–5先备一个例，pp.6–9解释轨道blow-up和周期扰动各自用途。无附录/独立结语。P4 §7.4保留不能由低计数开环语言实现的反例，附录F保留共同达到障碍，不以“未加强主定理”删除。**比较**：P4这些反例的目的现在明确；该文单一问题更易快速把握，P4整体阅读负担仍高；构造角色的说明有所接近，但体系、贡献和非自治设定不能直接比较。没有照搬作者稿的压缩或措辞。

**8. Gao, S., Jacoby, L., Johnson, W., Leng, J., Li, R., Silva, C. E., & Wu, Y. (2025).** On finite spacer rank for words and subshifts. *Discrete and Continuous Dynamical Systems, 45*(1), 248–285. https://doi.org/10.3934/dcds.2024092

[出版记录](https://www.aimsciences.org/article/doi/10.3934/dcds.2024092)；[全文作者稿](https://arxiv.org/pdf/2010.05165v4)，2024-06-26，35页全部阅读（稿内6月27日）。§1 pp.1–2用Morse/Sturmian问题区分rank；§2 pp.3–5交替放定义和具体词，前缀异常解释proper条件；§3 pp.9–19多种准则各有对象；§4 pp.19–23区分词与系统；§5 pp.23–28作Sturmian构造；§6 pp.28–29先示意错位出现，再定义expected occurrence，pp.30–34给准则和例，无附录/独立结语。P4 §6.4将实现结论从四项列表改为连续陈述；C的三组准则按任务取舍，未假称数学重复。**比较**：两稿都需要精细对象区分，P4未必较差于其全部定义铺陈，也没有全篇更好的证据；P4新增的算子用途说明减少了局部跳跃；rank新概念与反馈优化的贡献不可比。

**9. Chandgotia, N., Marcus, B., Richey, J., & Wu, C. (2026).** Shifts of finite type obtained by forbidding a single pattern. *Discrete and Continuous Dynamical Systems, 48*, 538–576. https://doi.org/10.3934/dcds.2025152

[出版记录](https://www.aimsciences.org/article/doi/10.3934/dcds.2025152)；[全文作者稿](https://arxiv.org/pdf/2409.09024v1)，2024-09-13，38页全部阅读，图所在pp.8、17、37、38另作视觉检查。§1 pp.1–4从一个计数问题区分已知/新增；§3.1 pp.7–8解释图的记忆；§3.2 pp.16–18正文保留算法，附录pp.36–38证明所需验证；§4 pp.18–24的Example 4.12区分一种交换方法失败与任意共轭失败；§5 pp.25–29区分局部/全局可容许；§6 pp.30–35给有具体内容的问题。P4保留D完整实现、F指定类/全类界限；把独立矩阵分支留档而非将附录全删。**比较**：P4局部范围限制现在可定位；仍不像其单一核心禁词对象那样集中，但该文§6也较宽；D/F证明解释有所改善而技术负担仍在；分类/共轭问题与P4贡献不可直接排名。

**10. Arbulú, F., Durand, F., & Espinoza, B. (2024).** The Jacobs–Keane theorem from the S-adic viewpoint. *Discrete and Continuous Dynamical Systems, 44*(10), 3077–3108. https://doi.org/10.3934/dcds.2024052

[出版记录](https://www.aimsciences.org/article/doi/10.3934/dcds.2024052)；[作者发表记录](https://farbulu94.github.io/research.html)；[全文作者稿](https://arxiv.org/pdf/2307.10663v1)，2023-07-20，32页全部阅读（稿内7月21日）。§1 pp.1–3分已知Jacobs–Keane结论和新的刻画；§2.6–2.8 pp.7–9解释tower/address/adapted概念用途；§3 pp.13–16矩阵分解后给超出经典准则的例；§4 pp.16–22先说明纤维控制目标，Lemma 19分解为通向投影与测度估计的claims；§5 pp.22–23主证明简短依赖这些准备；§6.1 pp.23–24将已知Dekking结论作为恢复的推论，后续例分开不同蕴含，无附录/独立结语。对应P4容量证明三步、5.6推论及F先说明构造目的。**比较**：已知工具与贡献的区分现已更接近；P4仍有两条不同机制，难达其主刻画的集中程度；定义前说明用途改善局部可读性，但该文早期多态射例也增加负担，不全盘模仿；其测度和零测集处理不能移作实际支撑下界。

**综合判断。** P4目前能明确给出问题、两条路线各自所得及未解决的共同采样环节；这些组织功能已接近上述参照。不能据此说它比十篇整体更好。主要不足仍是框架跨度较大、C/D/F技术阅读负担高，以及一般L/M问题仅部分解决。后者是贡献范围，不是英文润色可补齐的结论。没有总分、AI率或发表保证。十篇仅用于组织比较，未作为装饰引用加入论文；涉及数学的原有归属保留。

## 3. 全部42个原编号结果及主要辅助内容的取舍

“留档”指从本轮论文撤下，完整证明仍在保留的52页TeX/PDF中，不是判其错误。新稿34个编号结果，31个proof环境；没有为凑数制造结果。逐项核对标签和正文依赖，无保留证明依赖已撤下的八项。5.6由theorem改corollary、C.1由theorem改proposition，数学陈述不变。

| 旧结果 | 新稿去向与具体理由 |
|---|---|
| 2.1，物理标签合并 | 2.1；有限控制全类极小化的必要约化，不能省 |
| 2.2，物理/观测标签区别 | 2.2；说明单个细分规则的计数可能变化，限定2.1的用途 |
| 3.1，闭安全覆盖公式 | 3.1；共同后继路线的主结论 |
| 3.2，柱拼接 | 3.2；给3.1下界所需的任意长间隔独立选择 |
| 3.3，Borel/范畴桥梁 | 3.3；从分割非第一纲原子到可拼接开集，核心依赖 |
| 3.4，覆盖/名字间隙 | 3.4；已有三符号例的解释任务，不能以覆盖数替代名字数 |
| 3.5，控制系统推论 | 3.5；将3.1应用到真实安全块反馈，保留其推论地位 |
| 3.6，不同后继边界 | 3.6；说明共同后继假设不可直接删，并引出容量路线 |
| 4.1，产品容量定理 | 4.1；第二条主路线，仅定M，未扩大为共同A |
| 4.2，实际纤维容量 | 4.2；将产品估计接到全状态名字，核心依赖 |
| 4.3，循环置换推论 | 4.3；沿用早期系统而改后继，说明安全覆盖与真实反馈不同；M精确，L只给界 |
| 5.1，删除坐标估计 | 5.1；共同采样构造的有限损失控制 |
| 5.2，可数语言共同达到 | 5.2；回答容量路线留下的一类共同时间问题 |
| 5.5，固定语言达到 | 5.5；5.2的直接应用，保留简短形式 |
| 5.6，可数语言极小极大 | 5.6，改推论；直接来自同时达到，不再呈现为并列新主定理 |
| 5.7，clopen可数性 | 5.7；给5.6可核验的应用类 |
| 6.1，全周期塌缩 | 6.1；说明固定控制周期的必要性，直接由Kawan构造得到 |
| 6.2，符号到控制实现 | 6.2；6.4及F的实际全类投影依据，完整证明保留，陈述合并 |
| 6.3，Thue–Morse精确率 | 6.3；提供同一实际系统的连续/稀疏分离并被F使用 |
| 6.4，零不变性熵/正稀疏率 | 6.4；解释为什么传统不变性熵不能回答本问题，是直接推论 |
| 7.1，整数仿射吸收 | 7.1；体积界可达到的基准，含非一致等待和全部周期 |
| 7.2，保护逆支 | 7.2；在同一采样下为每个反馈实现全部字，解释比纤维体积更强的机制 |
| 7.3，密度一采样 | 7.3；四分支系统一类固定采样的精确答案，为D/E提供比较 |
| 7.4，交替语言无Borel实现 | 7.4；阻止把低计数开环覆盖当成反馈上界，保留有用反例 |
| A.1，整数对数量化 | A.1；保留已知归属及完整有限集合证明，支持极小值达到 |
| A.2，最小值达到 | A.2；解释inf何时可写min，不与固定A达到混淆 |
| B.1，加权Sauer估计 | B.1；给单步条件显式独立坐标比例，作为主定理的定量补充 |
| B.2，临界边界 | B.2；严格条件不能放宽的具体反例，紧接B.1 |
| C.1，严格源列权准则 | C.1，改命题；保留精确矩阵表示后的一个一般应用及全参考概率障碍 |
| C.2，跨层分散准则 | 旧C.2留档；非严格一步预算靠跨层损失收缩，有独立价值，但非保留证明依赖；主文3×3例已解释产品优势 |
| C.3，gain–loss准则 | 旧C.3及表格/实例留档；允许增益且无共同非增左权，是进一步矩阵族分析，不是C.1的同义结果，但使反馈主线分叉 |
| E.1，实际加权模式对 | E.1；精确说明体积估计丢失斜率、相容对和覆盖重叠三类信息 |
| E.2，可数修改满支撑 | E.2；既阻止无条件正修正，又说明几乎处处相同不足以确定计数，不能删 |
| F.1，整数额外扩张/连续因子 | 旧F留档；考察未被主定理假定的因子排除变体，7.1的基准计算及3.6边界均不依赖它 |
| G.1，有界正密度障碍 | 旧G留档；研究换参考测度能否挽救某个标量测试，非现行固定Lebesgue比较所需；不声称任意满支撑问题已解决 |
| H.1，抽象不可数障碍 | F.1；先说明可数性为何有内容，同时保留其不是动力控制反例的限制 |
| H.2，稀疏子移位族 | F.2；F.3实际连续有限控制构造的必要引理，先讲两个目标再给幂四编码 |
| H.3，四控制点态障碍 | F.3；区分指定族不共同达到与全类L=M，直接限定5.6的解释 |
| I.1，有限切换 | 旧I留档；处理名字族切换闭合，是独立问题；D已对真实贪心任意等待给直接计数，不调用此引理 |
| I.2，等待一步 | 旧I留档；说明固定稀疏序列对一个等待步骤敏感，有价值但非当前任何证明前提 |
| J.1，Shannon/密度一边界 | 旧J留档；排除一种概率替代，现稿未作该替代；E.2在目标四分支系统中承担所需支撑区别 |
| J.2，碰撞容量边界 | 旧J留档；二阶概率量与支撑的另一个独立失败，非E.2的等价命题，也非主定理工具 |

其他内容的决定：§3周期二精确采样例保留，解释“每个A”和“可选A”不同；§4平滑密度峰、3×3产品和Φ的实际反馈保留，分别分离固定测度标量测试及全部满支撑单步测试。C保留有限柱**全范数精确**表示，不能写成有限截断数值证据。D保留真实贪心全部上界和逆路径下界，不裁掉端点与无限延续；E开头保留算术采样次乘性和两个inf交换，解释有限块优化能给什么。旧F的tent局部扩张反例、旧G的参考概率/Lipschitz共轭讨论及C/I/J的附带讨论随各自分支留档。5.3/5.4关于limsup和闭包无限见证的remarks仍保留，它们防止实际误读。§6经典比较、符号实现、Thue–Morse并不重复：依次回答定义关系、如何实现、为何严格分离；只合并铺陈和列表，不撤掉证明。

此前六组补回内容逐一追踪：物理标签区别→2.2；循环系统→4.3；加权实际模式对→E；指定十块种子→继续留在更早旧稿；条件返回证书→继续留档；有限切换/等待一步→本轮由旧I留档。没有自动恢复既往探索内容。

## 4. 五处真实改写前后

以下取自旧/新TeX，省略的数学公式用位置说明，不伪称全文差分。

**1. 算子为何控制列表计数。** 原文只说跟随分支，随即给范数；读者尚不知道重复质量为何允许、范数在计数中做什么。新版先展开两步，再说明它是特定反馈列表纤维的上界。

改前：
```tex
Fix $2\le k\le q$ and set $l=k-1$. A list $S\subset W$ has
$l$ labels and is chosen independently of the state. The sum
$A_S=\sum_{u\in S}L_u$ follows every allowed branch in that
list. We use
```

改后：
```tex
Fix $2\le k\le q$ and set $l=k-1$. For a list $S\subset W$
of $l$ labels, let $A_S=\sum_{u\in S}L_u$. For example, two
successive lists $S_0,S_1$ give
\[
 A_{S_1}A_{S_0}\one
   =\sum_{u\in S_0,\ v\in S_1}L_vL_u\one.
\]
Each summand carries source mass through one safe two-block path.
Different paths may carry the same source mass, so the sum is an
upper bound on the mass following those lists under a particular
feedback. Its $L^\infty$ norm also bounds its integral. This is the
quantity that will control the size of a list box in the counting
argument. For arbitrary lengths put
```

**2. 容量证明的转折。** 原有概述已有主要步骤，但没有明确区分统一质量估计和依赖反馈的位置选择。新版强调真实纤维覆盖Q为何迫使很多列表盒，再由有限引理取独立坐标，同时交代依赖反馈的是哪一步。

改前：
```tex
Here is the idea. Allow a fixed list of $k-1$ controls at each of $n$
successive block times. If the total mass that can follow these lists
is at most $b_n$, covering all the actual names requires at least
$1/b_n$ list boxes. Exponential decay of $b_n$ then forces large
independent sets of coordinates by a finite combinatorial lemma.
The definitions below make this estimate uniform over the feedback.
```

改后：
```tex
The counting argument has three steps. First we bound the mass of
initial states that can follow a prescribed list of $k-1$ labels at
each time. Since the fibers of any feedback cover $Q$, many such list
boxes are needed to cover its names. A finite covering lemma then turns
this large covering number into a set of positions on which all choices
of $k$ labels occur. Only this last set of positions depends on the
feedback; the mass estimate will hold uniformly over all safe rules.
```

**3. 直接后果的地位。** 旧theorem标题让读者把此处看作又一独立主结果。新版改corollary并将适用语言条件放在一起，保留原量词和证明。

改前：
```tex
The elementary minimax inequality gives only
\begin{align*}
 \sup_A\inf_{\C\in\mathfrak C}\hseq^A(\C;Q)
 \le\inf_{\C\in\mathfrak C}\sup_A\hseq^A(\C;Q)
 =\inf_{\C\in\mathfrak C}\hpat(\C;Q).
\end{align*}
Separate maximizing schedules for separate partitions do not give the
opposite inequality. The next theorem obtains it by constructing one
sequence that attains every individual rate.
```

改后：
```tex
The simultaneous-attainment theorem applies once there are only
countably many such languages, up to renaming their letters. Taking
infima along its common sequence gives the reverse of the elementary
minimax inequality. This yields the following direct corollary.
```

**4. 稀疏族为何这样编码。** 原文从构造记号开始，读者不知幂四和参数树用途。新版先说每个族成员要在自己的位置上复杂、共同固定位置上典型地简单，再解释两点确定平移。

改前：
```tex
Write $\Theta=\{0,1\}^{\N}$, with its fair Bernoulli probability
$\nu$. For a finite binary word $v$, including the empty word, set
```

改后：
```tex
We need an uncountable family of shift-invariant languages with two
features. Each language must contain full binary patterns on its own
sparse set of positions, but a fixed sampling sequence should see few
of those positions for most parameters. We encode a parameter by a
branch of the binary tree. Powers of four place its nodes so that a
pair of positions determines their translation uniquely.

Write $\Theta=\{0,1\}^{\N}$, with its fair Bernoulli probability
$\nu$. Let $\operatorname{val}_2(v)$ be the integer represented by
the binary word $v$, with value zero for the empty word. Set
```

**5. 四控制构造各部分做什么。** 原文直接给空间和映射。新版先分配Thue–Morse分量、稀疏分量和寄存器的任务，让后续乘积与全类/指定族比较可跟随。

改前：
```tex
\begin{proof}
Let $Z$ be the Thue--Morse subshift of
Section~\ref{sec:thue-morse}, and let
```

改后：
```tex
\begin{proof}
The first control component will be forced by a Thue--Morse state;
this fixes the full-class minimum at $\log2$. A second component
can record one of the sparse languages above, raising individual
maximal-pattern rates without permitting one sequence to attain them
all. A register makes the two choices physically distinct controls.

Let $Z$ be the Thue--Morse subshift of
Section~\ref{sec:thue-morse}, and let
```

摘要另外重写为“共同观察序列能检测什么”的问题；引言不再平行宣传三种矩阵族；§3复用§2计数约定；§5.2把安全、有限见证、无限延续、闭包有限模式依次连接；§6.1从同一个覆盖数解释三种时间选择；§6.4把符号实现的四项罗列合为结论和直接后果；§7开头解释各仿射例的不同任务；§8只保留共同采样的具体障碍。终读再将“Changing the sampling period”改为“Changing the control period”，在E.1补首次出现的G_w复合定义，在F.2定义val₂及空词值。这些是理解和表述修正，不是新定理。

## 5. 受影响数学的核验与界限

重新核对修改涉及的定义、结论、完整证明和依赖；没有以旧通过标签、有限检验或a.e.结论充当数学理由。

- **真实反馈与覆盖**：Borel原子上有限块拼接仍为Borel映射；块内每个中间时刻安全，块末回Q后重复同一规则，给无限延续。原子细分比较通过物理标签投影；闭安全域子覆盖只用于构造实际选择器，未把开环覆盖直接作为其名字上界。
- **共同后继**：至少r个非第一纲原子、混合柱拼接及开放映射下第一纲逆像依赖齐全。分割依赖的阈值与预给渐疏A兼容，不交换inf与极限。尺度1和1/τ明确分开。
- **容量**：L_u来自安全纤维推前；源纤维限制的丢弃只增密度。乘积顺序、全局固定列表、全部安全门保留。真实非空零测纤维也计名字；1≤总容量来自全域覆盖，再用列表覆盖界和Kerr–Li有限引理。统一的质量界不产生统一位置集，未推出一般L=M。
- **有限柱/权重**：正算子产品的L∞范数在1上达到，而1的迭代在所给有限维空间中，故C的矩阵表示对全长度精确。共同正左权是源列预算，不能当作更换参考概率的右权。严格源列条件中的上界方向及θ<1保留，非任意Borel反馈被强加柱可测性；全参考概率的反证仍用支撑分离和正重叠。
- **语言与同时达到**：删除有限旧坐标的损失有明确分母代价；阶段终点可随语言，结论仍是各自limsup，不偷换共同收敛。名字闭包的每个有限模式有真实柱见证，不声称每个无限闭包名字有单一Borel见证。5.6只对固定τ及可数语言类。
- **经典比较/符号实现**：Kawan公式及归属保留，有限时域闭安全集合的有序差给Borel分割；spanning次乘和无限值情形均保留。变控制周期只是inf恒等式，不是跨周期同一个物理A。符号投影的满射由紧致性和被迫物理标签证明，不由Borel原子闭性推出。Thue–Morse的显式有限字见证完整保留。
- **仿射/贪心/加权对**：整数吸收包括任意长等待与右端点；保护逆支在所有端点合法且可无限延续；D的上界不误称禁词语言全部可实现，下界通过同一贪心反馈逆路径实现。E只数同一初态的偶奇对，N/W/Z次乘来自真实轨道分裂而非自由拼接；两个inf交换不是交换极限或得到统一极小化反馈。三修正项方向及逆覆盖长度等式保留，新定义G_w消除首见记号缺口。可数修改在除去可数初态后的整条轨道相同，仍能改变全部初态的有限支撑。
- **F的不可数障碍**：参数ν-a.e.估计用于找到某个参数；对每个被选参数仍数所有状态的实际模式，没有丢掉“零测状态”。四控制构造全类值log2与指定四标签族log4分开；点态共同达到失败不是全类极小极大失败。保留所有实现证明和这一限制。

没有发现保留且受影响论证中尚未修复的具体证明缺口；这不是形式化验证、外部审稿或作者已经审阅的声明。主定理、必要假设、量词、适用类和数值均未改变。已知量化/覆盖工具准确归属，AI使用说明逐字保留；不虚构AI使用仅限语言润色。因旧C.2/C.3留档，删除不再使用的Shi2021引用；共同正左权保留Debauche等归属。其余11项文献保留，十篇比较文章未装饰性加入。

四分支系统仍是M₁=log2，log(3/2)≤L₁≤log2，log(3/2)≤ℓ₂≤ℓ₂ᴬ≤logρ，h_A₂(s_g)=logρ，ρ⁶=ρ⁵+ρ⁴+ρ+1，logρ=0.55600938749…；循环系统M₁=log2而L₁只有原上下界；保护系统L₁=M₁=log3；整数系统为logm；共同后继为logr/τ。没有把贪心精确值宣称为最佳偶采样反馈值。

## 6. 最终检查、剩余问题与停点

脱离研究日志从标题至附录连续读完最终稿，处理上述首次定义和控制周期措辞后再次编译。latexmk/pdfLaTeX实际输出42页，157个唯一标签、34个编号结果、31个proof环境、11项文献；全部引用/交叉引用解析，无编译警告、Overfull/Underfull、越界文字或无效页跳转。42页全部渲染并视觉检查，长公式、表格、编号和末页正常。页面检查不代替数学证明。

**写作**：反复重启定义、并列准则目录、缺少对象用途和独立附录分叉已作实质处理。没有看到仍需机械替换的一类固定套话，不能因此宣称“AI感消失”。C的源列不等式、D的有理端点逆路径和F的参数稀疏族仍是具体阅读难点；它们目前具有目的说明和完整依赖，但没有独立专业读者的试读证据。重复提醒尽量收在其必要位置，不能再为流畅删掉全类/子类等条件。

**正确性/未解研究**：本轮没有已知未修复的受影响证明缺口。一般共同采样、四分支精确L₁和偶采样最优性、一般参考概率及既往留档的实现/返回问题仍未解；后两类不再分散现行正文。它们不是因本轮省略而缺掉的已知证明。2002b继续“未取得、未核实，获取关闭”。

**贡献**：论文有明确的共同后继精确结论、容量充分条件及区分机制的例子，但没有一般全反馈极小极大分类。若评价认为这一贡献范围不足，继续加小命题或改英文无法补救。本轮没有资格保证DCDS接受，也没有证据宣布整体优于十篇参照。由作者判断这些现有结果是否足以组成一次投稿；本轮不投稿、不选刊、不联系他人、不启动新研究。

**停点**：本次修订交付后不自动再开同样的对照轮次。已清楚且有完整证明的3、4、5节主体及必要反例应停止机械换词；后续若有真实读者的具体卡点，再按该段数学任务处理，而不是宣称读者反馈已不存在。

## 7. 保存与提交核验

仅新增本报告和DCDS TeX/PDF，更新CURRENT、README、NEXT_COMMAND并在VERIFICATION尾部追加§73。其原956700字节前缀SHA-256必须保持`2d098bf603ca7d6cd670dec14901e38d0255fcf62104811e51e176f42e0e9dc3`；其余33份基线文件逐字保留，包括52/57/56/60/54页稿和原稿。原稿SHA-256保持`c38552174b2fb0dee04ed56038952437f3e3ec3bd3725a5b1ace7812703f81ed`。

提交前再核main，用基线为唯一父和base tree，expected_sha非强制更新。提交后按返回的实际SHA全文回读7份新增/修改及33份保留文件，核字节、SHA-256、Git blob、父提交、树、main及历史前缀；实际提交和回读结果随交付给出，不在包含自身的报告里预填未来SHA或预称尚未执行的检查完成。仅P4/R02；未分派代理、读改P3/P6、重启暂停问题、R03或增长分类。
