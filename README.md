# P4：Sparse Sampling and Inverse Capacity in Safe Feedback Systems

**当前主要阅读版本：2026-10-09 的 47 页完整英文审阅稿。** 本轮已完成数学、可读性与学术表达的实际审查和修订，基线 main 为 `b544a2ceeb583208082c09b92bfeb2e497302968`。

- [最新论文 PDF](upgrade/R02/P4_REVIEWED.pdf) / [TeX](upgrade/R02/P4_REVIEWED.tex)
- [审查记录、精简问题清单及逐条证明依赖](upgrade/R02/MANUSCRIPT_REVIEW.md)
- [当前状态](CURRENT.md) / [后续停点](upgrade/R02/NEXT_COMMAND.md)
- [完整核验记录，最新第 67 节](upgrade/R02/VERIFICATION.md)

核心结果研究两种不同优化：安全逆列表产品的统一收缩给出全部合法 Borel 反馈的最大模式阈值和精确 M；有限闭覆盖在混合单边有限型系统上的计数定理，则给每个预设渐疏序列的全 Borel 细化精确值，并用于共同后继系统。有限柱应用包含严格左权重、跨层分散和允许增益列的损失补偿。产品定理没有自动解决一般共同采样问题。

本轮重建全部 33 项编号结论及附录关键推理，未发现需撤回主定理或改动既有数值的实质错误。已修复定义缺项、补全实际纤维与相位前缀推理、明确 E.2 完整逆分支和单点边界，并纠正一处不变性方向用语。摘要、引言和章节顺序实际重写，容量主定理提前至第 8 页。完整证明、原稿保留结果、必要反例和未解边界均在。

编译、引用和全部 47 页检查完成。Kerr–Li/Huang–Ye 的组合输入、HMY 的共同正阈值及既有正矩阵方法准确归属。AI 使用说明仍如实包含数学辅助，没有改成仅语言润色或虚构作者已审阅的承诺。该稿可供导师/同行完整审阅，尚非作者确认的投稿终稿。

## 保留版本和记录

- [48 页整合 PDF](upgrade/R02/P4_INTEGRATED.pdf) / [TeX](upgrade/R02/P4_INTEGRATED.tex) / [当时的整合说明](upgrade/R02/INTEGRATION_NOTES.md)
- [原稿](original/P4_FINAL.tex)
- [九页候选 TeX](upgrade/R02/P4_REVISED.tex) / [PDF](upgrade/R02/P4_REVISED.pdf)
- [R02 研究](upgrade/R02/RESEARCH.md) / [R01 研究](upgrade/R01/RESEARCH.md)
- [十篇论文学习记录](upgrade/R02/FOUR_MAJOR_STUDY.md)
- [原候选投稿信](upgrade/R02/COVER_LETTER_DRAFT.md) / [声明草稿](upgrade/R02/AUTHOR_DECLARATIONS_DRAFT.md) / [清单](upgrade/R02/SUBMISSION_CHECKLIST.md)

这些保留文件没有被本轮审阅稿覆盖；旧投稿材料没有自动适配新版本。VERIFICATION 第 1–66 节的 917,253 字节保持原样，仅追加第 67 节。原稿 SHA-256：`c38552174b2fb0dee04ed56038952437f3e3ec3bd3725a5b1ace7812703f81ed`。

共同采样、原 Q=[0,6] 精确数值、Y/H 和其他暂停分支不自动重开。2002b 保持“未取得、未核实，获取关闭”。只处理 P4/R02；未投稿、未联系他人、未分派代理，未评定期刊档位。
