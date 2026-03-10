# Survey Matrix

## Reordered Matrix

The matrix below follows the scientific workflow rather than the historical maturation order of AI systems. Notably, data analysis agents emerged earlier as an engineering capability through code execution, notebook interaction, and tabular analysis, but are placed after experimentation here to align the taxonomy with the logic of research practice rather than technical genealogy.

| Automation Depth \\ Research Task | Literature Discovery & Synthesis | Hypothesis / Research Design | Experimentation / Execution | Data Analysis | Reproducibility / Verification | Scientific Communication | Cross-Task / End-to-End |
|---|---|---|---|---|---|---|---|
| Tool-level Assistance | STORM, Co-STORM | AutoSurvey |  | DS-Agent |  | PaperX |  |
| Workflow-level Orchestration | DeepResearcher, OpenResearcher, ReportBench, ResearcherBench, DeepResearch Bench II |  |  | DSBench, DataSciBench, KramaBench | Scaling Reproducibility |  | scitex-python |
| Long-horizon Research Agent | OpenResearcher | AI co-scientist | SciDER |  | PaperBench, ScienceAgentBench, CORE-Bench |  |  |
| Closed-loop / Autonomous Research |  | The AI Scientist, AI Scientist-v2 | autoresearch |  |  |  | FARS, The AI Scientist, AI Scientist-v2 |

## Note on scitex-python

`scitex-python` is best placed in `Workflow-level Orchestration x Cross-Task / End-to-End` because its main contribution is modular tooling and full-pipeline orchestration rather than autonomy in a single research subtask.
