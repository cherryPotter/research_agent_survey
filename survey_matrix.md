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

## Notes on placement

### Why add a separate figure / visual communication column?
Recent systems explicitly target scientific **figures**, **posters**, and **image editing / rendering** rather than pure text generation. Keeping them inside a generic “Scientific Communication” bucket hides an important emerging sub-area.

### What counts as “figure / visual communication” here?
- **General-purpose image generation / editing useful for research visuals:** `Nano Banana 2`
- **Scientific figure generation:** `FigGen`, `FigAgent`, `SciFig`, `AutoFigure`
- **Academic illustration / method diagram agents:** `PaperBanana`
- **Poster generation:** `Paper2Poster`

### Why keep `scitex-python` under Cross-Task / End-to-End?
`scitex-python` is best placed in `Workflow-level Orchestration x Cross-Task / End-to-End` because its main contribution is modular tooling and full-pipeline orchestration rather than autonomy in a single research subtask.

### Optional systems you may also want to mention in the surrounding survey text
- [IDRBench](https://www.researchgate.net/publication/399707921_IDRBench_Interactive_Deep_Research_Benchmark) for **interactive** deep research evaluation.
- [Benchmarking LLMs in Scientific Discovery via Inspiration Retrieval, Hypothesis Composition, and Hypothesis Ranking](https://arxiv.org/abs/2503.21248) for a more fine-grained look at **hypothesis-generation** evaluation.
- [Agentic AutoSurvey](https://arxiv.org/abs/2509.18661) and [AutoSurvey2](https://arxiv.org/abs/2510.26012) as follow-up systems if you want the survey-writing thread to extend beyond the original `AutoSurvey`.