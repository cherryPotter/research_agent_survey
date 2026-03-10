# Survey Matrix

## Reordered Matrix

The matrix below follows the scientific workflow rather than the historical maturation order of AI systems. Notably, data analysis agents emerged earlier as an engineering capability through code execution, notebook interaction, and tabular analysis, but are placed after experimentation here to align the taxonomy with the logic of research practice rather than technical genealogy.

To cover the visual side of scientific communication, I split the original `Scientific Communication` column into **textual communication** and **figure / poster / visual communication**. This makes room for recent systems focused on method figures, posters, and controllable research graphics (e.g., Nano Banana 2, PaperBanana, FigAgent, SciFig, and Paper2Poster).

| Automation Depth \\ Research Task | Literature Discovery & Synthesis | Hypothesis / Research Design | Experimentation / Execution | Data Analysis | Reproducibility / Verification | Scientific Communication (Text) | Figure / Poster / Visual Communication | Cross-Task / End-to-End |
|---|---|---|---|---|---|---|---|---|
| Tool-level Assistance | [STORM](https://storm.genie.stanford.edu/), [Co-STORM](https://storm-project.stanford.edu/research/co-storm/) | [AutoSurvey](https://arxiv.org/abs/2406.10252), [AI co-scientist](https://arxiv.org/abs/2502.18864) |  | [DS-Agent](https://arxiv.org/abs/2402.17453) |  | [PaperX](https://arxiv.org/html/2602.03866v3) | [Nano Banana 2](https://blog.google/innovation-and-ai/technology/ai/nano-banana-2/), [FigGen](https://arxiv.org/abs/2306.00800) |  |
| Workflow-level Orchestration | [DeepResearcher](https://github.com/langchain-ai/open_deep_research), [OpenResearcher](https://arxiv.org/html/2408.06941v1), [ReportBench](https://arxiv.org/abs/2508.15804), [ResearcherBench](https://arxiv.org/abs/2507.16280), [DeepResearch Bench II](https://arxiv.org/abs/2601.08536), [DeepScholar-bench](https://arxiv.org/html/2508.20033) |  |  | [DSBench](https://arxiv.org/abs/2409.07703), [DataSciBench](https://openreview.net/forum?id=BltaWJZMeR), [KramaBench](https://arxiv.org/html/2506.06541v1) | [Scaling Reproducibility](https://arxiv.org/abs/2602.16733), [CORE-Bench](https://arxiv.org/abs/2409.11363) |  | [Paper2Poster](https://paper2poster.github.io/), [SciFig](https://arxiv.org/html/2601.04390v1), [AutoFigure](https://huggingface.co/papers/2602.03828) | [scitex-python](https://github.com/ywatanabe1989/scitex-python) |
| Long-horizon Research Agent | [OpenResearcher](https://github.com/GAIR-NLP/OpenResearcher) | [AI co-scientist](https://research.google/blog/accelerating-scientific-breakthroughs-with-an-ai-co-scientist/) | [SciDER](https://arxiv.org/abs/2603.01421) |  | [PaperBench](https://arxiv.org/abs/2504.01848), [ScienceAgentBench](https://github.com/OSU-NLP-Group/ScienceAgentBench), [CORE-Bench](https://arxiv.org/abs/2409.11363) |  | [PaperBanana](https://arxiv.org/abs/2601.23265), [FigAgent](https://www.researchgate.net/publication/400780235_FigAgent_Towards_Automatic_Method_Illustration_Figure_Generation_for_AI_Scientific_Papers) |  |
| Closed-loop / Autonomous Research |  | [The AI Scientist](https://arxiv.org/abs/2408.06292), [The AI Scientist-v2](https://arxiv.org/abs/2504.08066) | [autoresearch](https://github.com/karpathy/autoresearch) |  |  |  | [Nano Banana 2](https://aistudio.google.com/models/gemini-2-5-flash-image) | [FARS](https://analemma.ai/fars), [The AI Scientist](https://sakana.ai/ai-scientist/), [The AI Scientist-v2](https://github.com/SakanaAI/AI-Scientist-v2) |


- [SciAgentGym: Benchmarking Multi-Step Scientific Tool-use in LLM Agents](https://arxiv.org/pdf/2602.12984v1)
SciAgentGym，里面集成了 1,780 个带类型签名的领域工具，覆盖 物理、化学、生命科学、材料科学 四个方向；然后基于这个环境做了 SciAgentBench，包含 259 个任务、1,134 个子问题，并且分成从简单动作到长程工作流的多级难度。

即使是领先模型，随着交互步数增加，成功率也会明显下降；文中给的例子是 GPT-5 从 60.6% 掉到 30.9%，整体成功率也只有 41.3%。这说明现在真正卡住 scientific agents 的，往往不是“不会做一步推理”，而是不会跑完整条 workflow

- [S1-NexusAgent](https://arxiv.org/abs/2602.01550): 把“长程科研 agent”做成一个可自我演化的系统

multidisciplinary scientific research 里最难的几个问题：
长程规划、工具编排、长上下文管理、以及执行后如何从轨迹里持续学习。论文里最核心的设计是一个 hierarchical Plan-and-CodeAct 范式，把“全局科研规划”和“局部子任务工具执行”分成双层循环；系统还原生支持 MCP，并且可以接入成千上万的跨学科工具。

不是只做 benchmark，这篇最值得拆开的三块是：

hierarchical planning：全局研究计划和局部执行分层；
context/object management：不是把所有中间结果都塞回 prompt；
trajectory-to-skill distillation：把成功轨迹变成下次可直接调用的技能。

- [Scaling Reproducibility](https://arxiv.org/abs/2602.16733)
人类先固定诊断模板，AI 只负责获取材料、解析规格、重建环境、执行代码、生成标准化报告