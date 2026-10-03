# P4 R02 停点核验：证明通过，原文缺口部分缩小，继续暂停

日期：2026-10-03（Asia/Shanghai）。核验基线：`23ed9c0e4b4168904eab11c14a4b9c7eeedad030`。本文件是 R02 的后续核验，不启动 R03，不替换 R02 原研究记录。

**裁决。** R02 的同控制块原子合并命题、四控制系统及其全部 Borel 类的精确熵计算，通过本次从定义出发的复核。没有发现改变这些结论的数学错误。补写了三项定义层面的细节：闭包不增加有限模式、模式增长极限存在、稀疏生成族已经闭。文献方面首次读到 Kamae 上传的 2002a 早期作者稿的相关正文，并定位旧 Toeplitz 证明的修正线索；关键最终出版版及其他原文仍有缺口。

**一般数值极小极大问题仍未决定。** 本次没有获得作用于全部安全选择器的一般采样机制、全类严格缺口或重大结构后果。保持当前四大升级路线及整篇重写的暂停，不以一次方法失败推断 P4 永远不能升级，也不转成普通期刊整理。

## 1. 恢复、读取与保留范围

本轮指令中的 `khdzzg5shnt-rgb` 来自上一条助手拟定指令的拼写错误。沿用已核实的恢复提交所在仓库 `khdzg5shnt-rgb/p4sida`；没有访问或修改其他研究仓库。

启动时 GitHub `main` 恰为核验基线，没有后续实质进展；递归树没有 `AGENTS.md` 或 `VERIFICATION.md`。本地工作目录及各父目录未发现适用 `AGENTS.md`。已全文读取当前 `CURRENT.md`、`upgrade/R02/RESEARCH.md`、`upgrade/R02/NEXT_COMMAND.md`，并定向回查 R01 的定义和原稿中的文献编号。远程 R02 研究记录 blob 为 `b2213cae74ea803d254544e5099774f3ddf8be48`，与本地全文一致。

唯一原稿 `original/P4_FINAL.tex` 的远程 blob 为 `03564feac83b763fabb0d84a5cdb13afca6ca4a8`，本地仓库副本与本轮附件均为 58,870 字节，其 SHA-256 均为：

```text
c38552174b2fb0dee04ed56038952437f3e3ec3bd3725a5b1ace7812703f81ed
```

本轮保留原稿、R01 两份文件和 R02 `RESEARCH.md` 原样；只新增本文件并更新 `CURRENT.md`、`README.md`、R02 `NEXT_COMMAND.md`。未读取其他附件的论文正文，未混入 P3、P6。

## 2. 先固定对象，避免名字闭包与熵极限的隐含前提

时间为 `N_0`，控制空间是全部 `U^{N_0}`。`X` 紧致度量，`U` 有限非空，各 `f_u` 连续，`Q` 非空紧致且控制不变。固定正整数周期 `τ`，令 `W=U^τ`。`φ(j,x,w)` 表示依次使用 `w` 的前 `j` 个控制后的状态。

一个合法分割 `C=({D_i}_{i=1}^q,τ,ν)` 是有限非空 Borel 原子对 `Q` 的分割，每个原子指派控制块 `ν(D_i)∈W`，且

$$
\forall i\ \forall x\in D_i\ \forall j\in\{0,\ldots,\tau\},
\quad \varphi(j,x,\nu(D_i))\in Q.
$$

反馈块映射为 `T_C(x)=φ(τ,x,ν(D_i))`。实际名字 `ι_C(x)_k=i` 当且仅当 `T_C^k(x)∈D_i`。定义 `M_C={ι_C(x):x∈Q}` 和 `Σ_C=closure M_C`。`T_C` 不必连续；`Σ_C` 仍是有限字母乘积空间中的非空紧致前向移位不变集合，因为 `σι_C(x)=ι_C(T_Cx)`。

**有限见证。** 对每个有限 `F⊂N_0`，都有 `Σ_C|_F=M_C|_F`。若一个有限模式属于闭包，指定该模式的柱集是开集且与闭包相交，必与 `M_C` 相交。反向包含显然。这里仅需要每个有限模式分别有状态见证，不能宣称一条闭包名字总有同一状态的无限见证。

令 `P_C(F)=#(Σ_C|_F)`，`p_C^*(n)=max_{|F|=n}P_C(F)`。最大值存在：所有计数是介于 1 和 `q^n` 的整数。拆分任意 `n+m` 元坐标集得

$$
p_C^*(n+m)\le p_C^*(n)p_C^*(m).
$$

Fekete 引理给

$$
h_*(C)=\lim_n\frac{\log p_C^*(n)}{n\tau}
=\inf_{n\ge1}\frac{\log p_C^*(n)}{n\tau}.
$$

严格递增序列 `A=(a_i)⊂N_0` 上定义 `F_n={a_1,…,a_n}` 和 `h_A(C)=limsup_n log P_C(F_n)/(nτ)`。直接有 `h_A(C)≤h_*(C)`。本次没有将固定序列的 `limsup` 擅自改成极限，也没有用一般量化定理替代后文的直接计算。

令 `𝒜` 为全部这样的采样序列，`𝔠_Bor(Q,τ)` 为全部合法有限 Borel 安全分割。原候选一的普遍命题是：对每个满足上述假设的系统和每个固定 `τ≥1`，是否有

$$
\sup_{A\in\mathcal A}\inf_{C\in\mathfrak C_{\rm Bor}(Q,\tau)}h_A(C)
\stackrel{?}{=}
\inf_{C\in\mathfrak C_{\rm Bor}(Q,\tau)}h_*(C).
$$

左侧不超过右侧由逐成员上界直接成立。这里问的是数值等式，并未要求同一个 `A` 对每个 `C` 达到该成员自己的 `h_*(C)`。第 6 节只在一个具体周期一系统中证明等式，不将其外推到所有系统或所有周期。

## 3. 同控制块原子合并：全部内层下确界精确不变

对 `w∈W`，定义

$$
K_w=\bigcap_{j=0}^{\tau}\{x\in Q:\varphi(j,x,w)\in Q\},
\qquad g_w(x)=\varphi(\tau,x,w).
$$

各 `K_w` 闭。控制不变性及完整控制序列空间给 `⋃_{w∈W}K_w=Q`；枚举有限的 `W`、依次取差，已给一个 Borel 安全选择器，故合法类非空。

给定任意 `C`，合并同块原子为 `E_w=⋃_{ν(D_i)=w}D_i` 并删去空集。它们构成 Borel 安全分割 `C'`，且 `E_w⊂K_w`、`T_{C'}=T_C` 逐点成立。有限字母映射 `π(i)=ν(D_i)` 满足 `M_{C'}=π^∞M_C`。连续性给一个闭包包含方向，`π^∞Σ_C` 的紧致闭性给另一方向，故

$$
\Sigma_{C'}=\pi^\infty\Sigma_C,
\qquad \forall F\text{ 有限},\quad P_{C'}(F)\le P_C(F).
$$

因此对每个 `A`，`h_A(C')≤h_A(C)`，并有 `h_*(C')≤h_*(C)`。合并类是全类的子类；每个全类成员又有一个熵不增的合并成员，两个方向的不等式证明每个内层下确界完全相等。

于是全类问题可以精确写为满足 `x∈K_{s(x)}` 的 Borel 函数 `s:Q→W`。任意两个合法选择器在任意 Borel 子集上拼接仍合法。这是对**全部**安全分割和混合的化简，而不是只处理一个列出的策略族。它不保证选择器可数、策略空间紧致或 `T_s` 连续。该命题通过。

## 4. 稀疏语言的独立重建及一个补写事实

取 `Θ={0,1}^N`，公平 Bernoulli 概率 `μ`。令 `j(v)=2^{|v|}+val_2(v)`、`b_v=4^{j(v)}`，空词也包括在内；`D={4^j:j≥1}`，`B_θ={b_{θ|ℓ}:ℓ≥0}`。不同正差值表示唯一：由 `4^j-4^i=4^{j'}-4^{i'}>0` 的 4-adic 赋值先得 `i=i'`，再得 `j=j'`。

设 `G_θ` 是所有支撑包含于 `(B_θ+t)∩N_0`、`t∈Z` 的二元序列之并，`Y_θ=closure G_θ`。

**补写事实：实际上 `Y_θ=G_θ`。** 若 `y∈Y_θ` 有至少两个一，固定其位置 `r<s`。每个覆盖这两个位置的前缀都在某个生成序列中出现。差值唯一性迫使所有这些见证使用相同的幂对及同一平移 `t`。再对任一其他一的位置取足够长前缀，得它也属于 `B_θ+t`。所以整个支撑包含于这一平移，`y∈G_θ`。零个或一个一的序列本来就在 `G_θ` 中。反向包含由定义成立。

该事实只加强定义核查，不作原创定理或重大进展。特别地，移位对应 `t→t-1`，前置零对应 `t→t+1`，直接得 `σY_θ=Y_θ`。逐坐标置零仍合法。

有限模式的一的位置集 `S` 若至少含两点，一对坐标差唯一决定候选结点对和平移；其他一再决定结点。若这些结点不兼容，则出现参数集为空；若兼容，则是最深结点对应的参数柱。零/单个一的模式在全部参数出现。因此有限前缀语言关于参数局部常值，`θ↦Y_θ` Hausdorff 连续。语言束

$$
\mathcal E=\{(\theta,y):y\in Y_\theta\}
$$

闭且紧致：参数、状态同时收敛时，Hausdorff 连续性保证极限状态仍属于极限参数的语言。

在 `B_θ` 任意 `n` 个位置可自由放置二元模式，故 `p_{Y_θ}^*(n)=2^n`。长度 `N` 的平移区间中，`D` 的点数至多 `L_N=2+ceil(log_4(N+1))`，因 `k` 个幂的跨度至少 `4^k-4`。所以 `|L_N(Y_θ)|≤(L_N+1)N^{L_N}`（`N≥2`），普通词熵为零。

### 固定采样序列的量词和真极限

固定 `A` 后，令 `M_θ(F_n)=sup_t|F_n∩(B_θ+t)|`。至少两个交点的平移由某一坐标差唯一确定，至多 `binom(n,2)` 个候选，且这些候选只依赖 `F_n,D`，不依赖 `θ`。每个候选涉及至多 `n` 个结点；若一条分支包含至少 `k` 个，必包含其中一个深度至少 `k-1` 的结点。柱测度及联合界给

$$
\mu\{M_\theta(F_n)\ge k\}\le n^3 2^{-(k-1)},\qquad k\ge2.
$$

这些事件可测：对 `k≥2`，只需上述有限候选平移，每个候选涉及有限个参数柱。取 `k_n=ceil(6log_2(n+1))+2`，事件概率可求和。第一 Borel–Cantelli 引理给几乎处处最终 `M_θ(F_n)<k_n`，从而

$$
0\le\frac{\log P_{Y_\theta}(F_n)}n
\le\frac{\log(k_n+1)+k_n\log n}{n}\longrightarrow0.
$$

这是 `∀A，μ-几乎处处θ` 的陈述，例外集依赖 `A`。没有得到或使用 `μ-几乎处处θ，∀A`。正是这个依赖使逐策略共同达到可以失败。

## 5. Thue–Morse 共同最大化坐标的算术核验

令 `t_n=s_2(n) mod2`，`Z=closure{σ^nt:n≥0}`。给有限非空 `J⊂N_0` 和目标位 `ε_j`，取 `M=max J` 并延拓目标到 `0≤j≤M`。设 `R` 是其中零位数，取

$$
q=\sum_{\substack{0\le j\le M\\\varepsilon_j=0}}4^j
+(R\bmod2)4^{M+1}.
$$

`q` 的二进制一的个数为偶数。在单独加 `4^j` 时：目标为一则空的偶位变为一，奇偶翻转；目标为零则偶位的一进位到紧邻空奇位，一的总数不变。进位不会触及校正位，故 `t_{q+4^j}=ε_j`。这证明 `P_Z({4^j:j∈J})=2^{|J|}`；空集情形平凡。

用移位 `q+1`，在 `A_TM=(4^{i-1}-1)_{i≥1}` 的前 `n` 个坐标得到全部 `2^n` 模式。故该序列达到 `log2`，且 `p_Z^*(n)=2^n`。

Thue–Morse 替换的长度 `2^ℓ` 超块只有两种；长度 `N≤2^ℓ` 的因子最多跨两个相邻超块。至多四种超块对，每种至多 `2^ℓ` 个起点。取 `ℓ=ceil(log_2N)` 得 `|L_N(Z)|≤8N`。这些都是直接算术/替换证明，不以未取得的 2002b 原文为前提。

## 6. 四控制系统：全部 Borel 反馈的精确计算

取 `Q=Z×𝔈×{0,1}`（`𝔈` 为第 4 节语言束），`X=Q⊔{†}`，墓地点孤立，`U={0,1}^2`。对 `x=(z,θ,y,r)`、`u=(a,b)`，匹配 `a=z_0` 时取 `f(x,u)=(σz,θ,σy,b)`，不匹配时取 `†`；`f(†,u)=†`。

`Q,X` 紧致度量。每个控制的匹配区域闭开，在其中状态移位和寄存器赋值连续；墓地点也闭开。故各 `f_u` 连续，有限离散 `U` 使 `f` 联合连续。选择第一控制为当前 `z_0` 即可逐步保持安全，`Q` 控制不变。

**不同控制的准确含义。** 同一第一控制的两种 `b` 在匹配状态有不同寄存器后继；不同第一控制在适当状态一方安全、一方到墓地点。因此四个状态映射两两不同。但每个状态只有两个安全控制，另两个都到墓地点；不能把 R02 理解成“每点有四个不同安全后继”。这不改变原命题。

### 6.1 无遗漏地覆盖全部 Borel 类

任意合法周期一原子指派 `(a_i,b_i)`，必须满足 `D_i⊂{z_0=a_i}`。无论反馈怎样依赖 `θ,y,r` 或切换，第一状态坐标恒为 `σ^kz`。原子标签映射 `π(i)=a_i` 将每条实际名字送到其初始 `z`。反向任取 `z∈Z` 和其他状态坐标，其合法实际行程又给这个 `z` 的名字。因此

$$
\pi^\infty(\Sigma_C)=Z,
\qquad \forall C\in\mathfrak C_{\rm Bor}(Q,1)\ \forall F\text{ 有限},
\quad P_C(F)\ge P_Z(F).
$$

闭包方向由连续字母映射和 `Z` 闭性保证，不要求状态反馈连续。任意 Borel 混合和原子细分都在这个论证内。

按 `z_0=a` 的两个 clopen 原子指派 `(a,0)`，得到 `C_0`。其名字识别为 `Z×0^∞`，每个有限 `F` 的计数恰为 `P_Z(F)`。所以对每个 `A`，

$$
\inf_{C\in\mathfrak C_{\rm Bor}(Q,1)}h_A(C)=h_A(Z),
\qquad \min_{C\in\mathfrak C_{\rm Bor}(Q,1)}h_*(C)=\log2.
$$

用 `A_TM` 又得

$$
\max_A\inf_C h_A(C)=\log2,
\qquad \forall C,\quad h_{A_{\rm TM}}(C)\ge\log2.
$$

同一 `C_0` 达到每个内层下确界。这些结论直接由有限模式计数证明，不依赖 Huang–Ye 或 Gao 的一般量化结论。全部 clopen 类也有同样下确界。

长度 `N` 的开环控制串安全当且仅当第一控制串等于初始 `z` 的前 `N` 位，第二控制串任意。故 spanning 集的最小大小为 `|L_N(Z)|≤8N`，普通不变熵的归一化对数趋于零。没有混入邻域容许误差版或不确定系统的另一种不变熵。

### 6.2 四标签指定族，不能代替全类反例

对 `η∈Θ`，令 `s_η(z,θ,y,r)=(z_0,1_{θ=η}y_0)`。单点参数切片闭，坐标柱闭开；四个纤维 Borel，均安全且均非空。每个指派不同控制块，无法继续合并。

选择器忽略寄存器，反馈保持参数并移位 `z,y`，故实际名字恰为 `Z×Y_η`：在 `θ=η` 时两个状态坐标独立遍历这两个语言，其他参数只贡献已包含的全零第二串。因此

$$
P_{C_\eta}(F)=P_Z(F)P_{Y_\eta}(F).
$$

在 `B_η` 任意 `n` 个位置上，两层同时各有 `2^n` 模式；四字母上界给 `p_{C_η}^*(n)=4^n`，`h_*(C_η)=log4`。这是共同坐标见证，不是把两层的最大模式熵无条件相加。普通词数受 `8N(L_N+1)N^{L_N}` 控制，普通名字熵为零。名字语言族 Hausdorff 连续紧致；这不是未定义拓扑下的“策略族紧致”。

固定任意 `A`，第 4 节给第二层归一化对数对几乎所有 `η` 真正趋零。写第一层为 `u_n`、第二层为 `v_n→0`，才使用 `limsup(u_n+v_n)=limsup u_n`，得到

$$
\forall A,\quad
\mu\{\eta:h_A(C_\eta)=h_A(Z)\}=1,
\qquad h_A(Z)\le\log2<\log4.
$$

故不存在单个 `A` 逐策略达到所有这些成员各自的 `h_*`。但每个成员都支配 `Z`，每个固定 `A` 又有成员取等号，因而指定子类的数值缺口为

$$
\max_A\inf_\eta h_A(C_\eta)=\log2
<\log4=\min_\eta h_*(C_\eta).
$$

全类却包含 `C_0`，其数值等式已在 6.1 精确算出。四控制构造通过；**它反驳逐策略共同达到，不反驳一般全类数值等式**。

## 7. 文献新增核验、版本与实质缺口

### 7.1 DOI 核验与 APA 书目

本轮重新核对一手出版社页面；另实际读取 Crossref 注册接口核对 Huang–Ye、2002b、2006 Toeplitz 和 2025 加权文章的标题、作者、卷期页/文章号与 DOI。2002a 和 Kawan 的 Crossref 请求返回 429，改以 Cambridge、Springer 的原始书目核对，未把接口失败写成验证成功。

1. Huang, W., & Ye, X. (2009). Combinatorial lemmas and applications to dynamics. *Advances in Mathematics, 220*(6), 1689–1716. https://doi.org/10.1016/j.aim.2008.11.009
   - [Crossref 一手注册记录](https://api.crossref.org/works/10.1016/j.aim.2008.11.009)实际返回 200；[Huang 的机构发表页](https://faculty.ustc.edu.cn/huangwen1/en/zdylm/994149/list/index.htm)也列出此文。
   - 出版社正文访问 403；PDF 入口返回 200 的短 HTML 而非 PDF。作者机构列表没有取得正文附件，ResearchGate 页面明确无公开全文。Theorem 2.1 及精确假设仍未直接核实。
2. Kamae, T., & Zamboni, L. (2002a). Maximal pattern complexity for discrete systems. *Ergodic Theory and Dynamical Systems, 22*(4), 1201–1214. https://doi.org/10.1017/S0143385702000585
   - [Cambridge 原始书目](https://www.cambridge.org/core/journals/ergodic-theory-and-dynamical-systems/article/abs/maximal-pattern-complexity-for-discrete-systems/D23738707FB0E8028EECE890B500509D)核对完整出版信息。
   - **新增正文入口**：[Kamae 上传的公开作者稿](https://www.researchgate.net/publication/232025808_Maximal_pattern_complexity_for_discrete_systems)，页面标明上传于 2023-02-17。稿件有 21 页，首面标注“to appear”，不是最终 14 页排版。实际读取其窗口定义、§5 Theorem 5 陈述及相关证明段落、§6 Theorem 6 的陈述与模式增长证明。早期稿存在公式识别损坏；未取得可视觉核验的 PDF，也未逐字比较最终版。
   - 该稿 §5 已讨论无理旋转的闭集二元编码具有满模式增长；它不提供 P4 全类 minimax。不得把这种 Borel 编码现象整体宣传为新发现。对 Thue–Morse 幂坐标公式的最终版历史排重仍未完成。
3. Kamae, T., & Zamboni, L. (2002b). Sequence entropy and the maximal pattern complexity of infinite words. *Ergodic Theory and Dynamical Systems, 22*(4), 1191–1199. https://doi.org/10.1017/S014338570200055X
   - [Cambridge 原始书目](https://www.cambridge.org/core/journals/ergodic-theory-and-dynamical-systems/article/abs/sequence-entropy-and-the-maximal-pattern-complexity-of-infinite-words/A5C670E61A2427693183C271CD22341D)及 Crossref 相符。PDF 入口实际重定向到摘要页；仍未取得关键正文。没有从摘要重建证明。
4. Kawan, C. (2013). *Invariance entropy for deterministic control systems: An introduction* (Lecture Notes in Mathematics, Vol. 2089). Springer. https://doi.org/10.1007/978-3-319-01288-9
   - [Springer 图书](https://link.springer.com/book/10.1007/978-3-319-01288-9)及[第 2 章](https://link.springer.com/chapter/10.1007/978-3-319-01288-9_2)，pp. 43–87。
   - 本轮章页面可读摘要、部分注释和参考文献，未开放完整章节；章节 PDF 未取得。Google Books 只读到目录/书目，指定页的可访问模式失败。ResearchGate 图书页仍仅章摘要。Definitions 2.2、2.3、2.8、2.9，Theorem 2.3、Lemma 2.3 的全部原文仍未核实。
   - 已有学位论文的[机构 PDF 入口](https://opus.bibliothek.uni-augsburg.de/opus4/files/1357/Dissertation_Kawan.pdf)本轮返回 502；不能自动替代 2013 专著编号。
5. Gjini, N., Kamae, T., Tan, B., & Xue, Y.-M. (2006). Maximal pattern complexity for Toeplitz words. *Ergodic Theory and Dynamical Systems, 26*(4), 1073–1086. https://doi.org/10.1017/S0143385706000150
   - [Cambridge 原始书目](https://www.cambridge.org/core/journals/ergodic-theory-and-dynamical-systems/article/abs/maximal-pattern-complexity-for-toeplitz-words/39C431D1F9E1D9BB0D46514952B39AFC)与 DOI 注册相符，正文未取得。Crossref 将两位中文作者的姓名字段按另一顺序切分，APA 不机械照抄该字段；姓名采用 Tan/谭、Xue/薛，参照作者英文公开署名及[北航机构页](https://math.buaa.edu.cn/szdw1/azcck/js/xym.htm)、[华中科技大学数学学院师资页](https://maths.hust.edu.cn/szdw/szdw.htm)。
   - 它是以下 2025 作者稿指向的修正来源。当前只完成书目定位，没有认证修正证明。
6. Nie, X., & Huang, Y. (2025). Weighted sequence entropy and maximal pattern entropy. *Journal of Statistical Physics, 192*(5), Article 62. https://doi.org/10.1007/s10955-025-03445-6
   - [Springer 原始页面](https://link.springer.com/article/10.1007/s10955-025-03445-6)与 Crossref 相符；公开预览只含首页/导言开头。摘要声称 homeomorphism 下加权模式熵等于序列熵上确界。未读完整证明；没有把它推成安全选择器优化或另开加权路线。

### 7.2 一个实际查到的纠错线索及竞争范围

Le, A. N., Pavlov, R., & Schlortt, C. (2025). *On subshifts with low maximal pattern complexity* (arXiv:2508.13420v1) [Preprint]. arXiv. https://doi.org/10.48550/arXiv.2508.13420

本轮直接读取[作者稿 §2.2.2、Theorem 2.13 前后的说明及参考文献](https://arxiv.org/html/2508.13420v1)。它明确指出 2002a 中 simple Toeplitz 的证明有小错误，并指向上述 2006 文章的修正/推广。当前确认的是**2025 作者稿确有这项纠错说明**，不是本轮已审清 2002 最终版和 2006 修正的全部细节。它不涉及本文件的稀疏支撑概率估计或 Thue–Morse 算术证明。本轮未检索到独立正式勘误条目，不能据此说没有其他勘误。

其他竞争只核对新增版本/假设，不重复已覆盖的增长分类：

| 已有来源 | 本轮直接核对 | 限制 |
| --- | --- | --- |
| Gao、Ma、Rong、Tran，`arXiv:2310.05353`，DOI `10.48550/arXiv.2310.05353` | 一手版本页仍为 2025-04-03 v3。 | 沿用 R02 的相关证明阅读状态；未重读最终期刊版，不作为本次例子数值计算的前提。 |
| Li、Ouyang，`arXiv:2608.06103`，DOI `10.48550/arXiv.2608.06103` | 一手版本页仍只列 2026-08-06 v1；当前 HTML 仍以 homeomorphism 为系统约定，页眉为 2026-08-24。 | 本轮检查导言和假设，不认证全文；同版本号不能替代字节比较。 |
| Le、Pavlov、Schlortt，`arXiv:2508.13420` | 一手版本页仍为 2025-08-19 v1；新读到上述纠错说明。 | 不重新启动 pattern-Sturmian 分类路线。 |

检索还定向使用 `sequence entropy / minimax / control`、`maximal pattern entropy / Borel` 和 `common sequence / uncountable`。部分搜索返回无关实体，不能计为排重证据。已读到的相关来源仍没有提供 R01 的紧致指定族反例、R02 四控制全类计算或一般全选择器数值等式的直接证明。**这不是原创性认证；相关原始正文仍缺失。**

## 8. 证明修正范围、候选判断及停止条件

| 核验对象 | 本次裁决 | 精确边界 |
| --- | --- | --- |
| 选择器合并 | 通过 | 全部固定序列和模式下确界精确不变；不获得可数性或连续反馈。 |
| 语言束、控制连续性与安全性 | 通过 | 四映射两两不同；每点仅两个安全控制。 |
| 共同幂坐标及概率估计 | 通过 | 真极限趋零后再处理 `limsup`；几乎处处例外集依赖 `A`。 |
| 四控制全类数值计算 | 通过 | 两侧均为 `log2`，由同一 `C_0` 与 `A_TM` 给达到。 |
| 全类反例的解释 | 不成立 | 指定族存在缺口；全部 Borel 类在此例中没有缺口。R02 正文已经作此区分。 |
| R01/R02 原创性与精确历史归属 | 未核实完成 | 获得一份早期作者稿及纠错线索；其他关键最终版仍有缺口。 |

没有需要推翻的 R02 数学结论。需要补充的是上述定义证明和原文阅读状态，尤其不能继续把 2002a 写成“从未取得任何正文”，也不能升级为“最终版及所有公式均核验完成”。R02 `RESEARCH.md` 保留当时的历史状态，本文件及 `CURRENT.md` 给当前状态。

分别评价：

- **一般目标的重要性**：若成立，会回答固定周期下控制选择与采样选择的交换问题；目前没有可核实的重大未解问题或结构分类后果支持四大级判断。
- **实际新增的分量**：证明复核、三个辅助细节、作者稿补读和纠错线索。它们提高记录可信度，不构成新的升级核心定理。
- **证明可行性**：本例的强制 Thue–Morse 因子同时给下界和达到策略，故局部计算完整；一般系统未必有该因子或同一最小支配策略。未获得克服这一点的新机制。

因此保持暂停。后续只在有新的合法原文入口、具体纠错证据，或一个能作用于一般**数值等式**的新结构论证时做定向增量；无新证据不再重查本轮已经通过的证明，不自动开 R03，不加第三路线，不重写整篇，不降低目标。

## 9. 保存及回读约定

提交前检查相对链接、文本完整性与保留文件指纹；提交后按实际提交 SHA 回读本文件、三份状态/入口文件以及全部原样保留文件，并核对 `main`。提交 SHA 与实际回读结果在交付时给出，不将未来提交 SHA 写进自身。

## 10. 2026-10-03 正式原文增量：恢复 8903b72，仍保持暂停

本节是最新证据；第 7、8 节的文献未取得状态保留为上轮历史，不再代表下列四份来源的当前状态。本轮启动及写入前，`main` 都为 `8903b7200ff3599ef9ee14580cd668b68ee85786`，无后续实质进展；递归核对完整 Git tree，未发现 `AGENTS.md`。全文读取 CURRENT、本文件及 NEXT_COMMAND，按实际依赖回查 R01/R02 RESEARCH 和原稿。仅更新本文件及三份状态/入口文件，保留原稿与研究历史，不开 R03。

### 10.1 文件身份、完整性及实际阅读范围

盘点现有 14 份附件的首页/书目，优先读取以下四份。作者、题名、DOI、出版排版及首末页相符，连续出版页码未发现缺页。关键公式另作页面渲染核查，文件已上传不是正文已核验的依据。

| 用户文件 | 实际身份、版本和页码 | 已读范围及重点证明 |
| --- | --- | --- |
| `senquce (1).pdf` | Huang–Ye (2009)，*Combinatorial lemmas and applications to dynamics*，*Advances in Mathematics, 220*(6), 1689–1716；正式版，DOI `10.1016/j.aim.2008.11.009`；28 页连续。 | 全文读取；审查系统/覆盖定义、Theorem 2.1(1) 完整证明及 Lemma 5.1、Corollary 5.3、Theorems 5.4、5.5、5.9 的相关组合论证。不是对其所有元组理论及外部引理重新独立证明。 |
| `控制系统书.pdf` | Kawan (2013)，*Invariance entropy for deterministic control systems: An introduction*，LNM 2089，Springer，DOI `10.1007/978-3-319-01288-9`；PDF 共 290 页，目录、正文及末尾索引存在。 | 前置识别页及第 2 章全文，出版 pp. 43–87＝PDF 第 66–110 页，连续完整；重点审查 Definitions 2.1–2.3、2.8–2.9，Propositions 2.20–2.22，Lemma 2.3、Theorem 2.3 及数据率证明。不称全书证明已审完。 |
| `maximal-pattern-complexity-for-discrete-systems.pdf` | Kamae–Zamboni (2002a)，*ETDS, 22*(4), 1201–1214；Cambridge 正式 14 页版，DOI `10.1017/S0143385702000585`；不同于此前 21 页“to appear”稿。 | 全文读取；窗口/单词定义，§4 旧 Toeplitz 论证，§5 Theorem 5 闭集编码构造与证明，§6 Theorem 6 Tribonacci 数制证明。没有据此认证它所引用的 2002b 证明。 |
| `maximal-pattern-complexity-for-toeplitz-words.pdf` | Gjini–Kamae–Tan–Xue (2006)，*ETDS, 26*(4), 1073–1086；Cambridge 正式 14 页版，DOI `10.1017/S0143385706000150`；页码连续。 | 全文读取；重点审查 §2 Theorem 1、Corollary 1、Lemma 2 替代证明和 §3 满模式 Toeplitz 例子。未将全部分类结论当 P4 的依赖。 |

本次实际文件的 SHA-256（按上表顺序）：

```text
Huang–Ye 2009  03caefc1d87fe4be513211cdc6542a2cd74a48e806e538c70b0068545812c9f5
Kawan 2013     c68fe56fc0c76324bcb34a5c878c13d659741bc966a81e12f62cd3fb50c957b6
KZ 2002a       46d57d30ceac77ace75672a4174003e354b7b6d260c92610c032bf5f895dbbe7
GKTX 2006      182782065d5d7cf9fb38a4cbc43e2fb191950f5c1925b8b817f48f92319aa020
```

APA 书目采用 7.1 中已逐项核对的作者、卷期页和 DOI；现在这四项都有上述实际原文证据。Kawan 第 2 章独立 DOI 为 [10.1007/978-3-319-01288-9_2](https://doi.org/10.1007/978-3-319-01288-9_2)。未把 PDF 下载日期当成出版日期。

### 10.2 Huang–Ye：单覆盖达到及整数对数量化

**证据和量词。** pp. 1690–1693（PDF 第 2–5 页）给定义及 Theorem 2.1。一般 t.d.s. 约定为紧致度量空间上的 homeomorphism；对每个固定有限开覆盖 $\mathcal U$，Theorem 2.1(1) 给
$h^*_{\rm top}(T,\mathcal U)=\sup_A h^A_{\rm top}(T,\mathcal U)$，且该覆盖有一个达到序列。它是“每个覆盖各有一个序列”，没有控制选择器下确界的交换、全类统一阈值或逐策略共同达到结论。Borel 状态反馈产生的闭环未必连续，不能直接称为该 t.d.s.；须在适用的名字移位系统上使用结论。

**平移索引的完整补齐。** p. 1693 印出 $r_k=\max D_{k-1}+1$，不足以保证平移窗口有序且不重叠。定理可以直接修复：取近最大化窗口 $D_k$，$|D_k|=n_k$，令
$N_k=\sum_{i\le k}n_i$，使 $n_k/N_k\to1$ 且
$n_k^{-1}\log N(\bigvee_{t\in D_k}T^{-t}\mathcal U)\to h^*_{\rm top}(T,\mathcal U)$。
改取

$$
r_1=0,\qquad r_k=1+\max_{i<k}\max(D_i+r_i).
$$

令 $A$ 为各平移窗口并集的递增枚举，则前 $N_k$ 个位置恰为前 $k$ 块。覆盖细化及 homeomorphism 下最小子覆盖数的平移不变性给

$$
\frac1{N_k}\log N\!\left(\bigvee_{t\in A[1:N_k]}T^{-t}\mathcal U\right)
\ge\frac{n_k}{N_k}\frac1{n_k}
\log N\!\left(\bigvee_{t\in D_k}T^{-t}\mathcal U\right)\longrightarrow h^*_{\rm top}(T,\mathcal U).
$$

反向由最大窗口定义成立，证明完毕。这只补齐一个覆盖的串接；不外推到非满射语言，也不产生全选择器机制。原稿 A 的坐标删除论证保留，不修改原稿。

**量化的直接依据。** pp. 1709–1713（PDF 第 21–25 页）的有限模式组合证明给固定 clopen 分割 $h^*=\log j$（Theorem 5.4）。Theorem 5.5 明确用一侧子移位 $X\subset\{1,\ldots,m\}^{\mathbb N}$，给 $h^*(X)=\log j$，$1\le j\le m$；其有限坐标证明不需要逆移位，不能因导言的 homeomorphism 约定而漏掉这个表述。

用于安全选择器的名字闭包，并作 R02 同控制块合并后，

$$
h_*(s)\in\{\log j/\tau:1\le j\le |U|^\tau\}.
$$

所以非空全类的模式下确界达到。这补齐 R01 修正的 2009 正式原文依据；量化是已知定理，不另开增长路线。Theorem 5.9 的熵保持符号合并尚须控制实现接口，见 10.5。

### 10.3 Kawan：Borel 分割表示仍跨周期

Definitions 2.1–2.3（pp. 44–48）及 2.8–2.9（pp. 79–80；PDF 第 102–103 页）约定拓扑时间不变系统、可拼接控制、有限 invariant cover 及合法名字。指定控制须在整个 $[0,\tau]$ 保持安全，覆盖不要求开集。这里的覆盖熵按**连续**控制周期名字计数；离散信息率为 $\log_2$，P4 自然对数需乘 $\log2$。原稿已注明这个换算。

Propositions 2.20–2.22（pp. 79–81）以 spanning 控制拼接证明覆盖存在性、名字次乘性及
$h_{\rm inv}(Q)\le h(C;Q)\le\log\#\mathcal A/\tau$。
Lemma 2.3（pp. 81–82）按
$\widetilde A_j=A_j\setminus\bigcup_{i<j}A_i$
使覆盖互不相交，保留相应控制，所得合法名字包含于原名字；空片可删。这不是 R02 合并原分割中**同一控制块**的片：R02 后一种操作保持闭环轨道逐点不变，还给所有采样窗口的符号因子。两者不能写成字面同一引理，但因子计数本身也是基本事实，不支持重大新理论归属。

Theorem 2.3（pp. 82–83；PDF 第 105–106 页）给

$$
h_{\rm inv}(Q)=\inf_{C=(\mathcal A,\tau,v)}h(C;Q),
$$

$\mathcal A$ 可为 Borel 分割，**$\tau$ 也参与优化**。原文允许只考虑任意给定 $\tau_0$ 的整数倍，不是固定为一个 $\tau_0$。证明取 $\tau_k=k\tau_0$ 的最小 spanning 集（大小 $n_k$），以全程安全的 $G_\delta$ 片及有序差集构造 Borel 分割，再用

$$
h_{\rm inv}(Q)\le h(C_k;Q)\le\frac{\log n_k}{k\tau_0}\longrightarrow h_{\rm inv}(Q).
$$

这支持原稿所引用的已知跨周期表示，不解决固定周期模式 minimax。§2.4 的强不变性/开覆盖反馈熵（pp. 68–78）及 §2.5 数据率证明（pp. 83–87）同样没有把连续名字熵替换成固定周期模式熵，或对全部 Borel 反馈给共同采样阈值。第 2 章已全文读到，没有发现这里所需的交换机制。

### 10.4 2002a 的实际覆盖及 2006 Toeplitz 修正

**2002a 的覆盖。** pp. 1201–1203 定义含 0 的窗口和单词在所有非负平移处的模式；单词与其轨道闭包的有限模式相同，但这不把任意非传递语言束变成一条单词的轨道闭包。

Theorem 5，pp. 1208–1209（PDF 第 8–9 页），是“对**每个**无理旋转角，**存在**闭集 $S\subset[0,1)$，使 Lebesgue **几乎每个**初始点的二元编码对**每个** $k$ 有 $p_\alpha^*(k)=2^k$”。证明选择快速递减返回量 $\rho_i=\{q_i\theta\}$，以数位限制构造正测度闭集；每个目标模式的交集有正测度，再用遍历性及可数交集得到几乎处处结论。满模式增长的闭集/Borel 编码已经是已知现象。

§6 Theorem 6（pp. 1209–1213）实际处理 Rauzy/**Tribonacci** 替换及二元因子，用该数制的进位实现全二元模式，同时普通块复杂度线性。这覆盖低普通复杂度/满模式复杂度和进位造模式的一般背景，不是 P4 的控制优化定理。

正式 2002a 没有给出 Thue–Morse 定理或 P4 特定 $4^j$ 公式。原稿同时引用 2002a/2002b 且承认该复杂度是已知对象；现能确认 **2002a 单独不支持 Thue–Morse 精确归属**。2002b 是否支持或应改引另一原始来源，仍待正文核查。本文件第 5 节独立二进制证明不受出处缺口影响，不先猜缺失文章内容，不改原稿。

**直接纠错证据。** GKTX p. 1075（PDF 第 3 页）明确指出 `[KZ2]` 的 simple Toeplitz 证明错误，其参考文献中该项是 2002a。旧 §4 Lemma 2/Theorem 4（pp. 1206–1208）不能继续视为未经修正的可靠证明。本轮没有独立锁定旧论证唯一错行，也不擅自说其所有引理陈述均假。

**替代证明的完整核心。** GKTX Theorem 1、Corollary 1、Lemma 2（pp. 1076–1079；PDF 第 4–7 页）以常量模式补偿，证明二元 simple Toeplitz 对每个窗口 $F$ 有

$$
p_\alpha(F)-c_\alpha(F)+2\le2|F|,
$$

其中 $c$ 是常量词数。按 $k=|F|$ 归纳：$k=1$ 显然；$k=2$ 最多两个非常量词。合并 coding 开头同字母的层，写
$\alpha=(\eta\triangleleft\zeta)\triangleleft\beta=\xi\triangleleft\beta$，
$\eta,\zeta$ 的非孔字母分别全为 $a,b$，周期 $s,t$，合成周期 $r=st\ge4$。两种字母无限出现，尾词仍为 simple Toeplitz。

若 $F$ 占模 $r$ 的 $\ell\ge2$ 个余类，记余类窗口 $F_i$、缩小窗口 $\overline F_i$ 和余类集合 $L$，置

$$
D=|\pi_{\{a,b\}}F_\xi(L)|-2\ell,\qquad c'=c(\pi_{\{a,b\}}F_\xi(L)).
$$

Theorem 1 通过“各余类全常量”与“恰一个余类非常量”的不相交分解，给

$$
p_\alpha(F)-c_\alpha(F)+2\le D-c'+2+\sum_i p_\alpha(F_i).
$$

Corollary 1 给 $p_\alpha(F_i)=p_\beta(\overline F_i)+2-c_\beta(\overline F_i)$；各子窗口严格小于 $k$，归纳使和式不超过 $2k$。

为核实剩项，将 $L$ 按模 $s$ 分组为 $L_j$。每组投影除全 $a$ 词之外的模式数为
$|L_j|+\mathbf1_{\{|L_j|\ge2\}}$。
记 $1_a,1_b$ 表示两种常量词出现与否，则

$$
c'=1_a+1_b,\quad |\pi F_\xi(L)|\le1_a+\ell+\sum_j\mathbf1_{\{|L_j|\ge2\}},
\quad D-c'+2\le2-1_b-\lceil\ell/2\rceil\le0
$$

（$\ell\ge3$）。若 $\ell=2$ 且分在两个模 $s$ 组，指示项和为零，仍成立；若同组，投影为 $\{aa,ab,ba\}$ 或 $\{aa,ab,ba,bb\}$，均有 $|\pi F_\xi(L)|-c'=2$，故 $D-c'+2=0$。

若 $F$ 全在一个模 $r$ 余类，先利用 recurrence 平移使 $\min F=0$；Corollary 1 保持不变量：

$$
p_\alpha(F)-c_\alpha(F)+2=p_\beta(F/r)-c_\beta(F/r)+2.
$$

p. 1079 Case 2 印作反复除以同一 $r^e$；一般尾层周期可以变动，严谨写法是逐尾词重新分组取得 $r_0,r_1,\ldots$，累计除以 $R_e=\prod_{j<e}r_j\ge4^e$。若非零 $M=\max F$ 永远不进入多余类情形，就须对所有 $e$ 有 $R_e\mid M$，不可能。有限步后应用前一种情形，归纳完成。这补齐递归索引，不另声称发现正式新勘误。

上界已审清。原文再用非最终周期词 $p_\alpha^*(k)\ge2k$ 得等号；该周期判别是 2002a Theorem 1 **引用 2002b** 的结果，其原始证明仍缺，不能称整条外部依赖链都独立核实。

**P4 影响。** 稀疏支撑闭性/概率估计、Thue–Morse 进位不依赖旧 simple Toeplitz 证明或这个引用下界，R01/R02 既有数值不需修正。GKTX §3 Example 3（pp. 1084–1085）的满二元模式 Toeplitz 例子也不提供反馈优化，不恢复分类方向。

### 10.5 一般数值问题及实际验证的控制实现接口

记 $\mathscr S_\tau$ 为固定周期的**全部**合法 Borel 安全选择器，包含在任意 Borel 集上混合不同合法选择器。目标仍为

$$
L_\tau=\sup_A\inf_{s\in\mathscr S_\tau}h_A(s)\stackrel{?}{=}
M_\tau=\inf_{s\in\mathscr S_\tau}h_*(s).
$$

恒有 $L_\tau\le M_\tau$，右边因量化而达到；最小策略存在不意味着它的有限模式被所有其他策略支配。反向至少需要诸如
$\forall\varepsilon>0\ \exists A\ \forall s:\ h_A(s)\ge M_\tau-\varepsilon$。
单覆盖定理只给 $\forall s\ \exists A_s$，跨周期表示不保持这个固定 $\tau$。

**当轮验证一个决定性接口，给完整反例。** 新读 Huang–Ye Theorem 5.9(4) 保证熵保持的符号合并，但这不自动允许合并 R02 中不同控制块的原子。用原稿 C 已有的匹配控制机制作接口检验，不另加路线：

$$
Q=\{0,1\}^{\mathbb N_0}\cup\{2^\infty\},\quad
X=Q\sqcup\{\dagger\},\quad U=\{0,1,2\},\quad\tau=1.
$$

定义 $f(x,u)=\sigma x$ 若 $u=x_0$，否则进入固定墓点。$Q$ 紧致，首字母柱集 clopen，故各控制映射连续；安全反馈必且只能为 $s(x)=x_0$，已覆盖全部 Borel 类。每个 $n$ 元窗口有 $2^n+1$ 个模式，$h_*(s)=\log2$。

符号层把 $2$ 合入 $0$，因子恰为二元满移位，每个窗口有 $2^n$ 个模式，熵仍为 $\log2$。可是合并原子
$E=\{x:x_0=0\}\cup\{2^\infty\}$
没有共同安全控制：前一片只允许 0，后一片只允许 2，故
$\bigcap_{x\in E}\{u:f(x,u)\in Q\}=\varnothing$。
该熵保持因子不能实现为同一系统的合并安全分割，证明完毕。

反例阻断的是**符号因子到控制实现**的接口，**不是全类数值缺口**：本例对每个 $A$ 都有 $h_A(s)=\log2$，两侧相等。R02 相同控制块合并仍合法；跨不同块不仅须找到共同安全控制，改变闭环也不能自动声称名字是旧语言的符号因子。原文合并机制未跨过核心障碍。

| 对象 | 新原文实际覆盖与裁决 |
| --- | --- |
| 低普通熵、满模式熵及进位造模式 | 2002a/2006 已有背景现象；具体控制构造的精确历史排重仍未完，不认证重大原创性。 |
| R02 同控制块合并 | 相邻的覆盖互不相交化/符号因子已有基本理论；不是字面同一操作，不获得可数选择器类。 |
| 逐策略共同达到失败 | 单覆盖达到不给共同达到；R02 较强桥梁失败结果保留，不重复旧例核验。 |
| 指定子类缺口 | 不转换为全类反例；任意合法 Borel 混合仍须纳入。 |
| 四控制全类数值 | 仍为 $\log2=\log2$，指定子类才有 $\log2<\log4$。新增 Toeplitz 修正不影响该计算。 |
| 一般固定周期全类数值问题 | 未取得统一阈值采样、全类严格缺口或重大结构后果；仍未决定，原候选一保持暂停。 |

### 10.6 2002b 获取停点、版本及最终判断

仍缺的准确来源：

Kamae, T., & Zamboni, L. (2002b). Sequence entropy and the maximal pattern complexity of infinite words. *Ergodic Theory and Dynamical Systems, 22*(4), 1191–1199. https://doi.org/10.1017/S014338570200055X

14 份附件身份盘点没有对应全文，2006 Toeplitz 文不能替代。新增有界合法查找中，Cambridge 题名/作者/DOI 相符但 PDF 入口仍转摘要；ResearchGate 对应条目仅请求全文，没有公开附件；Kamae 作者主页入口访问失败。未从摘要重建证明，不循环已失败入口。已在聊天中**单独一条消息**请求用户补找完整出版版（或可识别完整作者稿），说明用途为原始序列熵覆盖、历史归属及获取缺口；这不阻断本轮其余工作。进一步明确它还用于核对 2002a 所引周期判别的原始证明。

另定位 Kamae–Salimov (2011)，*On maximal pattern complexity of some automatic words*，*ETDS, 31*(5), 1463–1470，DOI [10.1017/S0143385710000453](https://doi.org/10.1017/S0143385710000453) 的出版社书目；作者 PDF 入口未打开。仅是自动词归属待查线索，未读证明，不能说已支持 P4 的 Thue–Morse 公式，不因此增加路线。

仅复查既有竞争的一手版本页：Le–Pavlov–Schlortt `arXiv:2508.13420` 仍为 2025-08-19 v1；Gao–Ma–Rong–Tran `arXiv:2310.05353` 仍列 2025-04-03 v3；Li–Ouyang `arXiv:2608.06103` 仍仅列 2026-08-06 v1。没有将版本号未变视作字节相同，没有重启增长分类或认证全部竞争证明。2025 加权文章仍只核对书目/首页，不能由摘要加路线。

本轮修正的是**原文取得/阅读状态、索引写法及精确引用边界**；R02 数值不需修正。单覆盖串接、Toeplitz 递归补齐和符号合并控制实现接口反例都是实际增量，不是新的升级核心定理。没有跨过一般数值障碍的机制或四大级贡献重要性依据，继续暂停，不承诺成功、不降低目标。

下一轮只补真正新增的 2002b 正文、精确纠错证据或作用于一般全类数值问题的具体机制；不重复已补核四份原文，不开 R03，不恢复增长分类，不加路线，不重写整篇。原稿 SHA-256 再核仍为 `c38552174b2fb0dee04ed56038952437f3e3ec3bd3725a5b1ace7812703f81ed`；提交后按实际 SHA 回读四份更新文件及全部保留文件，未来提交 SHA 不写进自身。
