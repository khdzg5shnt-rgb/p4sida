# P4：十篇四大论文的定向学习

基线：main `8ab86501eed9e9f27d56c6694b5182fcb209e595`。记录日期：2026-10-06（Asia/Shanghai）。本次用户授权的是十篇论文学习，不是新一轮数学攻坚、改稿或投稿。

## 阅读范围与选文依据

已取得以下十篇的合法完整 PDF，核对正式发表身份与 DOI；实际精读引言、相关主命题及下表列明的证明。**不是十篇逐页通读或全部证明独立复核。** 页码均为所读取 PDF 的一基页码；作者版页码不能冒充期刊页码。未精读的应用、代数或分析技术不作为 P4 已核工具。

选文按 P4 的四个问题：预设采样的独立性、符号模型的真实实现、轨道改变后的结构控制、重叠造成的信息损失。三篇 Annals、五篇 Inventiones、两篇 JAMS；不为了平均分配期刊而加入不相关的 Acta 文章。这里是同方向及方法邻近的论文，**不是十篇已经研究了 P4 当前固定反馈问题的论文**。HMY、Huang–Ye、Kerr–Li 的既有直接背景仍保留，但非四大文章不计入这十篇。

| 编号 | 正式发表论文 | 与 P4 的联系 | 实际精读定位 |
|---|---|---|---|
| 01 | Rudolph–Weiss (2000), *Entropy and mixing for amenable group actions*, Annals | 直接联系：稀疏/分散采样的熵独立性 | PDF 1–10：引言、Definitions 2.4–2.5、Theorems 2.3/2.6/2.12/2.13、2.12 与主命题转移证明；17–19：2.11 证明；29–30：2.6 收尾及 4.10 |
| 02 | Boyle–Downarowicz (2004), *The entropy theory of symbolic extensions*, Inventiones | 直接联系：抽象熵约束怎样实现为实际符号模型 | PDF 1–4、16–27：Theorem 5.5；6.3/6.4；零维情形的双向证明、SWO 跨层分配、6.8/6.10 与熵计算 |
| 03 | Hochman–Shmerkin (2012), *Local entropy averages and projections of fractal measures*, Annals | 方法联系：复杂纤维投影的多尺度熵估计 | PDF 1–2、8–10、15–19、33–34：Theorems 1.9–1.13、树/树态射、Lemma 4.3、Theorems 4.4 与 8.1 的完整证明；8.2 只读声明和证明开头 |
| 04 | Lind–Schmidt (1999), *Homoclinic points of algebraic Z^d-actions*, JAMS | 结构联系：可求和轨道修正怎样产生真实拼接 | PDF 1–3、9–10、17–21：Lemma 4.5；specification 三种定义；5.3–5.5 和 Theorem 5.2 证明、5.7 边界 |
| 05 | Kerr–Li (2011), *Entropy and the variational principle for actions of sofic groups*, Inventiones | 框架联系：定义不变量、验证表示无关、连接数值理论 | PDF 1–6、24、35–37：微状态定义、拓扑定义、Theorem 6.1 及完整证明；生成序列无关的长证明未逐步复核 |
| 06 | Chung–Li (2015), *Homoclinic groups, IE groups, and expansive algebraic actions*, Inventiones | 结构联系：把独立性组织成内在对象和因子理论 | PDF 1–4、7–8、29–34：IE/measure-IE 定义、Theorems 7.3–7.4、Proposition 7.10 的完整证明；8.1 读声明，未复核其证明 |
| 07 | Seward (2019), *Krieger’s finite generator theorem for actions of countable groups I*, Inventiones | 编码联系：一个分割同时承担存储与可识别解码 | PDF 1–6、12–14、24–28：Theorem 1.1；Proposition 4.2；Lemmas 7.6–7.7 与 Proposition 7.8 完整证明；8.1 读声明 |
| 08 | Seward (2020), *Positive entropy actions of countable groups factor onto Bernoulli shifts*, JAMS | 编码/独立性联系：内部轨道排序及相对独立性转移 | PDF 4–6、15–16、27–35：Theorem 1.1；4.8–4.9；external past 定义与 8.2–8.5；9.1 的 Claims 1–6 证明。4.10 只读到第16页，未把它记为完整复核 |
| 09 | Gutman–Tsukamoto (2020), *Embedding minimal dynamical systems into Hilbert cubes*, Inventiones | 方法联系：动力一致的标记、重叠位置的编码资源分配 | PDF 1–6、22–27：Theorems 1.4/1.7、主结果归约；Voronoi tiling 的一致性、Lemmas 6.1–6.4 完整证明；最终插值嵌入证明未逐步复核 |
| 10 | Hochman (2014), *On self-similar sets with overlaps and inverse theorems for entropy*, Annals | 方法联系：低增长先推出结构，而非强迫无条件增益 | PDF 1–6、14–18、20–21、30–34、37–39：Theorems 1.1/1.3/1.4/2.7；Lemma 3.4；4.11 逆定理的组装证明；1.3 完整证明。4.6 的多重卷积分析未完整复核 |

## 逐篇学习：贡献、证明接口与 P4 限制

### 01：共同采样的量词要有可核证的来源

固定保测 amenable 群作用具有完全正熵时，分散有限时间集上的平均 Shannon 熵逼近分割的单次熵。2.12 用相对 K 性质与条件熵链式法则控制坏位置；2.11 的轨道转移使用 cocycle 和 uniform 集族。引言先对照已知 Z 情形，再说明转移的新困难。

**P4 判断：** 值得学的是“统一估计如何从假设推出”。固定作用、保测可逆轨道变化与任意 Borel 闭环不是同一对象；没有对全部反馈共同适用的测度与熵结构，不能用这篇替代全反馈共同采样证明。

### 02：覆盖、实现与最优值达到是三个不同问题

Theorem 5.5 用熵结构的有界仿射 superenvelope 刻画可实现的符号扩张熵函数。零维构造中的 SWO 不等式保证上一层编码容量足以容纳下一层且可一致解码，随后实际构造扩张并计算熵。论文将刻画、构造、不可达到边界放在同一理论中。

**P4 判断：** 最接近第42–43节的研究组织方式。不过，固定系统的扩张不是右逆截面；其 odometer/辅助系统也不能成为 P4 的额外相位或记忆。可以学跨层兼容证明，不能引用它宣告满覆盖语言可由反馈实现。

### 03：处理碎片纤维可以先保留条件信息

Theorem 4.4 对树态射构造随机测度：每个投影子纤维只保留一个孩子并接收该纤维质量，期望仍恢复原测度。局部熵与鞅差分把尺度信息转成投影维数下界；8.1 再连接 CP-chain。写法把一般接口与具体投影应用分开。

**P4 判断：** 这种随机纤维分解是分析工具，不是确定反馈构造；维数与采样模式数也不是同一指标。要迁移到 P4，仍缺对全部真实名字的定量局部熵条件及到模式总数的合法转换。

### 04：真实拼接来自可求和修正

Lemma 4.5 用 Fourier 逆构造基本 homoclinic 点；5.4 通过其可求和尾部控制不同轨道片段的相互误差。5.2 在 expansive algebraic Z^d 作用中联系完全正熵与多种 specification，并给出移除 expansiveness 后的边界。

**P4 判断：** 这解释了为什么“分支开放”不足以拼接：需要可定量控制的轨道修正。P4 当前闭环没有已核的群结构、固定 automorphism 或同态修正机制；不能重新套用已失败的共同轨道拼接桥梁。

### 05：数值理论先要有稳定定义和实现对象

该文将熵定义在近似等变的微状态空间，扩大此前有限生成分割框架，再建立变分原理。6.1 的反向不等式从大量分离微状态中抽取同一近似经验测度，以紧致性取得不变极限。引言清楚说明旧定义为何不能直接取所有分割的上确界。

**P4 判断：** 可学“定义—表示无关—数值联系—应用”的结构；这里的固定连续群作用和微状态极限不能交换 P4 的 sup_A 与 inf_s，也不能令随反馈变化的闭环自动满足同一个变分原理。

### 06：升级可以体现为独立性的结构刻画

7.3–7.4 把 IE 点组织成闭正规子群并刻画最大零熵因子；7.10 从轨道差异可求和，通过有限集分离与尾和估计实现正密度的全部标签模式。主结果明确比较已有 Z^d 理论和更一般群作用中新增的技术。

**P4 判断：** 重要启发是用内在对象解释信息在哪些方向可变化。IE 的正密度独立集、预设稀疏采样与对全部反馈一致下界不同；不能把 IE 非平凡直接写成 P4 的 log2 数值公式。

### 07：同一分割的自我解码要单独证明

主定理给定熵预算下的生成分割，且控制分布。7.6–7.8 明确设计互不冲突的标记与检查位置，再证明这些位置能从最终标签中识别；4.2 则将可数信息移入互斥存储区域。引言把“有限生成元存在”和“最优容量及分布控制”区分开。

**P4 判断：** 与同状态一致选控非常相关，但生成是 mod null sets，且作用由固定保测双射给出。P4 禁止遗漏特殊初态；不能用该定理直接补齐全域尾串一致性，也不能新增存储坐标。

### 08：独立性转移需要实际排序和条件信息

该文在固定作用内部构造轨道排序及 external past；8.4–8.5 证明内部 Z 作用与群作用之间的独立性、熵转移，9.1 再完成因子构造及等熵端点。其归约不是只说“有一个可测选码”。

**P4 判断：** 我们可借鉴“先建立相容排序，再转移信息”的证明顺序。内部变换允许沿原群轨道跳跃，结论保测且允许零测例外，不能替代 P4 固定周期的一步控制。全体遍历测度的陈述也不等于全部反馈的量词。

### 09：标记必须随动力学一致变化

该文把 minimal 系统的嵌入阈值从旧常数改善到最优 N/2。第6节从当前状态定义 Voronoi tiling，验证移位一致性；6.3–6.4 对短片段造成的编码缺口给出资源分配和等变权重。引言明确列出原界、锐界和新分析工具。

**P4 判断：** 最有用的是“相位在哪里可识别”必须证明。这里是固定 homeomorphism、marker property 与连续信号嵌入；P4 当前反馈改变未来，不能假定存在该标记，更不能把构造平面的坐标加进反馈状态。

### 10：低增长情形先做结构诊断

逆熵定理在卷积熵增益小的时候，将多数尺度分成近均匀或近原子的类型；局部平均及多次卷积把局部增益传到整体，再连接自相似重叠。引言精确限定所解的特殊情形，没有把全部 exact-overlap 猜想写成已经解决。

**P4 判断：** 可借鉴低模式数的结构诊断，但闭环偶/奇控制一般相关，不自动形成独立卷积。尚无合法的卷积表示及反馈无关参数，故不能用该逆定理提高现有 log(3/2) 下界。

## 对 P4 升级最重要的学习结论

以下是基于上述阅读的研究判断，不是文献定理，也不是已经完成的新证明。

1. **把最硬的兼容性问题放在主定理中心。** 第42节已有抽象覆盖与熵计算；第43节表明普通截面不够。真正的增量应解释何时能在原状态上同时做到合法选控、尾串一致和可计量的模式控制。继续只算另一种低熵语言，仍绕不开此处。
2. **扩展需要具体结构，而不只是更大参数。** 可核证的状态标记、有限错误的修复机制、可求和轨道修正或跨层容量分配，都是这些论文使用的具体内容。P4 目前尚未证明其中任一结构对全部目标反馈成立；应先核实一个接口，再讨论其适用范围。
3. **四大论文的写法服务于数学增量。** 这组论文通常先指出旧理论的精确局限，再陈述一个能跨过局限的定理，展示机制、重要后果和不可推广边界。不是所有论文都求解一般问题，但它们明确解释为什么所选系统类或新对象具有独立意义。这是本组样本的观察，不能当成期刊录用规则。
4. **量词和例外决定能否借用。** 固定作用的全部观察分割、同一作用的全部不变测度、所有反馈改变的闭环，是三个范围。a.e. 编码与全域编码是两种要求；维数、Shannon 熵、连续时间归一化、每个采样符号的模式熵也不能互换。

对下一次数学工作的建议：优先回到**动力一致的可识别编码位置**这一具体缺口，以02、07、09的兼容性证明作为比较对象。先检查这种结构能否由当前原状态及合法控制提供，且不依赖外部相位；不能在尚无结构时直接宣告有等变截面。01用于核查共同采样量词；03、10用于核查是否真的存在新增的定量增益。本次没有执行这些新尝试，也没有自动授权下一轮。

现稿第17节的闭覆盖公式、共同后继条件及第18节边界均不因本次阅读改变。第42节语言的全域实现仍未决定；两类固定偶数采样上界本次下降量为0；L1 的区间仍为 [log(3/2), log2]。阅读提供了比较标准和工具边界，**没有新增一区、一区Top或四大档位认证**。

## 正式引用、合法全文与版本

1. Rudolph, D. J., & Weiss, B. (2000). Entropy and mixing for amenable group actions. *Annals of Mathematics, 151*(3), 1119–1150. https://doi.org/10.2307/121130 。[期刊记录](https://annals.math.princeton.edu/articles/11136)；[完整PDF](https://arxiv.org/pdf/math/0005304)。所读32页带期刊页码1119–1150，来自该 arXiv 条目。
2. Boyle, M., & Downarowicz, T. (2004). The entropy theory of symbolic extensions. *Inventiones Mathematicae, 156*(1), 119–161. https://doi.org/10.1007/s00222-003-0335-2 。[作者完整PDF](https://terpconnect.umd.edu/~mboyle/papers/inventionesfinal31july03.pdf)，Date: July 31, 2003，共36页；不是43页出版社排版。正式卷年为2004，不用2003在线年份替代。
3. Hochman, M., & Shmerkin, P. (2012). Local entropy averages and projections of fractal measures. *Annals of Mathematics, 175*(3), 1001–1059. https://doi.org/10.4007/annals.2012.175.3.1 。[期刊记录](https://annals.math.princeton.edu/2012/175-3/p01)；[期刊完整PDF](https://annals.math.princeton.edu/wp-content/uploads/annals-v175-n3-p01-p.pdf)，59页。
4. Lind, D., & Schmidt, K. (1999). Homoclinic points of algebraic Z^d-actions. *Journal of the American Mathematical Society, 12*(4), 953–980. https://doi.org/10.1090/S0894-0347-99-00306-9 。[作者机构保存的期刊完整PDF](https://sites.math.washington.edu/~lind/Papers/HomoclinicPoints.pdf)，28页，首页有期刊、卷期和文章编号。
5. Kerr, D., & Li, H. (2011). Entropy and the variational principle for actions of sofic groups. *Inventiones Mathematicae, 186*(3), 501–558. https://doi.org/10.1007/s00222-011-0324-9 。[完整PDF](https://arxiv.org/pdf/1005.0399v3)，v3为2011-02-28、正文Date: February 21, 2011，共44页；不是58页出版社版。
6. Chung, N.-P., & Li, H. (2015). Homoclinic groups, IE groups, and expansive algebraic actions. *Inventiones Mathematicae, 199*(3), 805–858. https://doi.org/10.1007/s00222-014-0524-1 。[完整PDF](https://arxiv.org/pdf/1103.1567v3)，v3为2014-04-16，共49页；正式卷年2015，标题中的 groups 均为复数。
7. Seward, B. (2019). Krieger’s finite generator theorem for actions of countable groups I. *Inventiones Mathematicae, 215*(1), 265–310. https://doi.org/10.1007/s00222-018-0826-9 。[作者完整PDF](https://mathweb.ucsd.edu/~bseward/Files/krieger1.pdf)，34页；[作者发表目录](https://mathweb.ucsd.edu/~bseward/)确认期刊身份。文件未标明确切版本号，不猜测。
8. Seward, B. (2020). Positive entropy actions of countable groups factor onto Bernoulli shifts. *Journal of the American Mathematical Society, 33*(1), 57–101. https://doi.org/10.1090/jams/931 。[作者完整PDF](https://mathweb.ucsd.edu/~bseward/Files/sinai.pdf)，44页；[作者发表目录](https://mathweb.ucsd.edu/~bseward/)与[AMS文章记录](https://www.ams.org/journals/jams/2020-33-01/S0894-0347-2019-00931-8/viewer/)核身份；DOI、卷期页另核[Crossref注册元数据](https://api.crossref.org/works/10.1090%2Fjams%2F931)。2019在线发表与2020卷年区分；不把作者PDF猜作某个arXiv版本。
9. Gutman, Y., & Tsukamoto, M. (2020). Embedding minimal dynamical systems into Hilbert cubes. *Inventiones Mathematicae, 221*(1), 113–166. https://doi.org/10.1007/s00222-019-00942-w 。[完整PDF](https://arxiv.org/pdf/1511.01802)，38页。所读文件同时有 arXiv:1511.01802v1（2015-11-05）水印及内部 Date: September 17, 2018；如实保留这两项信息，不据此称为2020正式排版或断言逐字相同。
10. Hochman, M. (2014). On self-similar sets with overlaps and inverse theorems for entropy. *Annals of Mathematics, 180*(2), 773–822. https://doi.org/10.4007/annals.2014.180.2.7 。[期刊记录](https://annals.math.princeton.edu/2014/180-2/p07)；[期刊完整PDF](https://annals.math.princeton.edu/wp-content/uploads/annals-v180-n2-p07-p.pdf)，50页。所读为期刊原文，不用早期预印本替代。

前三类来源为出版社、作者机构站点及作者 arXiv 投稿。作者版与出版社版之间未完成逐字校勘；相应定理定位仅绑定所读文件。全文页数、尾部参考文献及文件可解析性已检查；关键 SWO 容量公式、Voronoi 移位关系、逆熵定理页面另经 PDF 渲染核查。没有将摘要、目录或“已下载”当成正文核验。

## 所读文件指纹

以下散列固定本次学习对象。全文只作临时阅读，仓库保存自己的学习记录与合法来源，不提交十份受版权保护的PDF。

| 编号 | PDF页数 | SHA-256 |
|---|---:|---|
| 01 | 32 | `a26c35bad6ecbc4df5c1a2803498f8e94f13b073ac732f1d57b0f02be364a2c4` |
| 02 | 36 | `26a3471bfeb0b7ad39be26c0abf59b451978f67694f60b26d1680d46c3f560bc` |
| 03 | 59 | `ffe34e1b8d1959fa81cf2beb3643a849f2b3c6ae0280bc15af97ea4be4f2611e` |
| 04 | 28 | `3884fb3c612883f458b694d62eba841af9325accae525d0a39a2e231bda69d9e` |
| 05 | 44 | `41032e098a1779e782b8546cbed75735bfb4a796f7d1a58934c865c354d5d591` |
| 06 | 49 | `325b42f3105ba66b7175ea63b53267f667ea5289c849916be00e8491ee6ede37` |
| 07 | 34 | `90a9f14f1a08c45eb27baf0115a3819cdfffd11c6c41cf6f92558f40e5536f22` |
| 08 | 44 | `67da2b359248da8924ac9b4be4c2b22a1656c5a472594f043362cc98986fb690` |
| 09 | 38 | `b74d0294e0b61e6c52b4251f315594814b0d4074ce550f8c9dbc133ce6867021` |
| 10 | 50 | `e50bcf12c8d854286031b108b47c36be281b8632c5041a471221293fd99287d0` |

原稿 SHA-256 保持 `c38552174b2fb0dee04ed56038952437f3e3ec3bd3725a5b1ace7812703f81ed`；既有正文、候选稿、投稿材料和R01/R02历史保留。2002b获取继续关闭；本次不处理该缺口、不认证原创性、不改任何数学数值。
