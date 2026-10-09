# P4当前状态：终审后的57页英文稿

更新：2026-10-10（北京时间）。本轮基线main为`cf1f8582ecb404535cca8e5bfbe225e27319388b`，树为`a667272a909b088dea6d0abc5a51f61d5c4f5380`；恢复时没有后续提交，适用目录和仓库树未发现AGENTS.md。

## 现行版本

- [57页现行PDF](upgrade/R02/P4_FINAL_REVIEWED.pdf) / [TeX](upgrade/R02/P4_FINAL_REVIEWED.tex)
- [完整终审报告](upgrade/R02/FINAL_PAPER_REVIEW.md)
- [保留的56页稿](upgrade/R02/P4_STYLE_REVIEWED.pdf) / [TeX](upgrade/R02/P4_STYLE_REVIEWED.tex) / [上轮报告](upgrade/R02/P4_MATH_STYLE_REVIEW.md)
- [保留的60页稿](upgrade/R02/P4_SELECTED_REVIEWED.pdf) / [TeX](upgrade/R02/P4_SELECTED_REVIEWED.tex)
- [保留的54页稿](upgrade/R02/P4_COMPLETE_REVIEWED.pdf) / [TeX](upgrade/R02/P4_COMPLETE_REVIEWED.tex)

全文已具有问题、贡献、两条证明路线、应用、边界反例及开放问题相衔接的研究论文组织。连续读取56页稿全部定义、结果、证明和未编号论证，独立复核关键依赖；旧标签不作正确性前提。没有识别出最终保留已证结论的未修复证明缺口，不等同于形式化验证、作者确认或同行审定。

本轮16处局部修订已落实：结尾的平滑例未解目标改为同一满支撑概率下最大两项容量之和<1；C.2的唯一合法控制限定为两A类；H.3补有限非零斜率分支条件；三处空窗口说明补齐。主定理假设和数值不变，局部条件确有澄清，不能统称所有假设逐字未改。

复用五篇JDE完整原文和已核记录，按问题重读相关位置；两篇出版版、三篇作者稿，后三篇最终出版版未逐字核对。引言提前解释与不变性熵的区别，删少量审计口吻及重复过渡，保留11节正文和8个附录。六组补回内容保留原分工，不新增成果或再次大规模重排。旧P4_MATH_STYLE_REVIEW四条摘要误述已在新报告§2.3勘误，旧文件保留。

实际编译57页并检查全部页面，197标签、48个编号结果、43个proof环境及12项文献保留，标签编号与56页稿一致；引用均解析，无编译/版式警告。46个编号环境、40个proof环境逐字不变，其余差异已复核。AI说明和参考文献逐字保留。

## 数值与停点

原Q=[0,6]仍M₁=log2、log(3/2)≤L₁≤log2、log(3/2)≤ℓ₂≤ℓ₂ᴬ≤logρ、h_A₂(s_g)=logρ及ρ⁶=ρ⁵+ρ⁴+ρ+1。循环例仍M₁=log2及log(q/(q−1))≤L₁≤log2；保护三分支例仍L₁=M₁=log3。未宣称一般L=M。

一般共同采样、精确L₁/偶采样优化、贪心最优性、十块覆盖的一致Borel实现、一般满支撑标量化、全反馈返回抽取及其他暂停分支未解决、未重启。2002b保持“未取得、未核实，获取关闭”。

已清楚的定理组织、必要限制、完整证明和有价值反例应停止机械修改。贡献强度及成果包取舍需要作者实质判断，不能由英文流畅或“像JDE”代替。不默认再开一轮同类审查，不提供AI检测率或发表保证。

## 保存和核验

新增FINAL TeX/PDF及FINAL_PAPER_REVIEW，更新本文件、README、NEXT_COMMAND，VERIFICATION仅追加第71节；其余27份基线文件字节和Git blob保持。原稿及54/60/56页等全部旧稿和记录保留。原稿SHA-256仍为`c38552174b2fb0dee04ed56038952437f3e3ec3bd3725a5b1ace7812703f81ed`；VERIFICATION前943930字节SHA-256仍为`493f30efe7cadbaa4e8546b469b9545400a03db5b123d7e040c629b23b540bd6`。

提交前复核main，使用实际base tree和expected_sha lease；提交后按实际SHA回读全部34文件，核父提交、树、main及保留字节。实际SHA和回读结果随交付提供，不预填未来SHA。仅P4/R02，无P3/P6读改、代理、新研究、R03、增长分类、选刊、投稿或对外联系。
