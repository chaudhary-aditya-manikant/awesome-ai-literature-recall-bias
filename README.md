# Awesome AI Literature Curation Bias

A curated collection of research papers, datasets, tools, implementations, and learning resources on **recall bias toward highly-cited and English-language papers in AI literature curation** — the systematic under-retrieval of relevant but less-cited, less-visible, or non-English AI research by search engines, scholarly recommenders, citation-graph tools, and LLM-assisted screening systems.

This repository accompanies an original research paper that develops the concept of "recall bias" as a testable framework for auditing AI-assisted literature discovery pipelines. It brings together the surrounding literature on citation bias, cumulative advantage, language bias, bibliographic database coverage, scholarly recommender-system bias, and automated screening, and organizes practical tools and datasets researchers can use to study or mitigate the problem.

## Contents

- [Overview](#overview)
- [AI-Assisted Research Paper](#ai-assisted-research-paper)
- [Citation Integrity Audit](#citation-integrity-audit)
- [Survey and Review Papers](#survey-and-review-papers)
- [Foundational Papers](#foundational-papers)
- [Recent Research Papers](#recent-research-papers)
- [Methods / Algorithms](#methods--algorithms)
- [Applications](#applications)
- [Evaluation Methods / Benchmarks](#evaluation-methods--benchmarks)
- [Datasets](#datasets)
- [Tools and Libraries](#tools-and-libraries)
- [GitHub Implementations](#github-implementations)
- [Tutorials and Learning Resources](#tutorials-and-learning-resources)
- [License](#license)

## Overview

AI research is increasingly discovered and filtered through search engines, citation graphs, scholarly recommender systems, and large language models rather than exhaustive manual search. These systems reduce the cost of navigating an exploding literature, but they can also reshape *which* papers become visible to reviewers, survey authors, and benchmark designers. This repository is organized around the concept of **recall bias**: a systematic gap in the probability that an otherwise-relevant paper is retrieved, ranked, screened, or retained, as a function of its citation prominence or publication language.

Two mechanisms are central. First, citation-based ranking and recommendation can reproduce cumulative advantage (the "Matthew effect"), so already-prominent papers keep gaining visibility while less-cited work stays buried even when it is substantively relevant. Second, English-language dominance in indexing, metadata, and retrieval infrastructure can systematically under-expose non-English scholarship, regardless of its quality.

The problem spans the full curation pipeline — indexing, candidate generation, ranking, screening, citation chaining, retention, and synthesis — and bias can enter at any stage. This collection gathers the empirical and methodological literature behind each stage, along with datasets, APIs, and open-source tools (citation graphs, active-learning screening systems, retrieval benchmarks) that researchers can use to measure, audit, or mitigate recall bias in their own AI-assisted review or discovery workflows.

## AI-Assisted Research Paper

**Recall Bias Toward Highly-Cited and English-Language Papers in AI Literature Curation**

This paper develops recall bias as a concept connecting citation bias, cumulative advantage, language bias, bibliographic database coverage, scholarly recommender-system bias, and automated literature screening. It proposes a framework for measuring group-conditional recall (recall stratified by citation percentile and publication language), reviews current human-AI and citation-network curation approaches, identifies methodological challenges — including the lack of a known relevant-paper denominator and the endogeneity of citation counts — and outlines future directions such as multilingual retrieval, popularity-blind re-ranking, citation-stratified evaluation, temporal audits, and transparent human-in-the-loop reporting.

[View Paper](paper/AI_Assisted_Research_Paper.pdf)

## Citation Integrity Audit

Every reference cited in the AI-Assisted Research Paper above was checked against its original source to confirm that it exists, is attributed to the correct authors and venue, and is characterized accurately (i.e., the paper's claims match what the cited source actually reports). The audit log documents each reference, its verification status, and any corrections made during drafting.

[View Audit](citation-audit/Citation_Integrity_Audit.pdf)

## Survey and Review Papers

- **Biases in Scholarly Recommender Systems: Impact, Prevalence, and Mitigation**
  Färber, M., Coutinho, M., & Yuan, S., 2023, *Scientometrics*
  [Paper / DOI](https://doi.org/10.1007/s11192-023-04636-2)
  Classifies popularity bias, selection bias, conformity effects, and Matthew effects in academic recommender systems — the direct scholarly-recommender analogue of the recall bias this repository is about.

- **Citation Recommendation: Approaches and Datasets**
  Färber, M., & Jatowt, A., 2020, *International Journal on Digital Libraries*
  [Paper / DOI](https://doi.org/10.1007/s00799-020-00288-2)
  Surveys citation-recommendation methods and datasets, providing the technical background for how citation-based ranking signals are built and where popularity can enter.

- **A Survey on Popularity Bias in Recommender Systems**
  Klimashevskaia, A., Jannach, D., Elahi, M., & Trattner, C., 2024, *User Modeling and User-Adapted Interaction*
  [Paper / DOI](https://doi.org/10.1007/s11257-024-09406-0)
  General recommender-systems survey showing popular items are systematically overexposed relative to long-tail items — the mechanism this repo's paper applies to scholarly search.

- **Predictors of Citation Rates and the Problem of Citation Bias: A Scoping Review**
  Lund, H., et al., 2025, *Journal of Clinical Epidemiology*
  [Paper / DOI](https://doi.org/10.1016/j.jclinepi.2025.112057)
  Scoping review of 165 studies and 54 predictors of citation rate, showing many predictors are unrelated to scientific quality — key evidence that citation count is a biased relevance proxy.

## Foundational Papers

- **The Matthew Effect in Science**
  Merton, R. K., 1968, *Science*
  [Paper / DOI](https://doi.org/10.1126/science.159.3810.56)
  The founding statement of cumulative advantage in scientific recognition — the theoretical basis for citation-driven recall bias.

- **The Matthew Effect in Science, II: Cumulative Advantage and the Symbolism of Intellectual Property**
  Merton, R. K., 1988, *Isis*
  [Paper / DOI](https://doi.org/10.1086/354848)
  Extends the Matthew effect concept to intellectual property and resource accumulation in science.

- **Collaborative Topic Modeling for Recommending Scientific Articles**
  Wang, C., & Blei, D. M., 2011, ACM SIGKDD
  [Paper / DOI](https://doi.org/10.1145/2020408.2020480)
  Foundational scholarly recommender system paper that explicitly notes citation-following is effective but biased toward heavily-cited work.

- **Introduction: Hegemonic Languages and Science**
  Gordin, M. D., 2017, *Isis*
  [Paper / DOI](https://doi.org/10.1086/694164)
  Historical account of how English became the dominant language of international science, framing the language-bias half of the paper's argument.

- **Scientific Citations Favor Positive Results: A Systematic Review and Meta-Analysis**
  Duyx, B., Urlings, M. J. E., Swaen, G. M. H., Bouter, L. M., & Zeegers, M. P., 2017, *Journal of Clinical Epidemiology*
  [Paper / DOI](https://doi.org/10.1016/j.jclinepi.2017.06.002)
  Meta-analysis of 52 studies showing statistically significant results are cited ~1.6x more often, establishing citation count as content-biased rather than a neutral quality signal.

## Recent Research Papers

- **Comparing Supervised Machine Learning and Large Language Models in Title-Abstract Screening**
  Aigner, M. F., Ganzinger, M., Probst, P., Rinckens, M., & Pausch, T. M., 2026, *Systematic Reviews*
  [Paper / DOI](https://doi.org/10.1186/s13643-026-03199-6)
  Directly compares LLM and supervised-ML recall on title/abstract screening, showing recall varies substantially by dataset.

- **The Use of Generative Artificial Intelligence in Systematic Literature Reviews: A Rapid Review**
  Fleurence, R. L., Qureshi, R., Aggarwal, R., et al., 2026, *Value in Health*
  [Paper / DOI](https://doi.org/10.1016/j.jval.2026.06.012)
  2026 rapid review of GenAI across systematic-review tasks, finding strong evidence for screening/extraction but caution against fully autonomous review generation.

- **Automated Citation Searching in Systematic Review Production: A Simulation Study**
  Rajit, D., Du, L., Teede, H., & Enticott, J., 2025, *Research Synthesis Methods*
  [Paper / DOI](https://doi.org/10.1017/rsm.2024.15)
  Simulates automated citation searching via OpenAlex and Semantic Scholar across 27 reviews, finding higher precision but significantly lower recall than manual searching.

## Methods / Algorithms

- **ASReview: Active Learning for Systematic Reviews**
  Van de Schoot, R., de Bruin, J., Schram, R., et al., 2021, Zenodo
  [Paper / DOI](https://doi.org/10.5281/zenodo.5126631)
  Open-source active-learning screening tool; illustrates how early-labeled examples can bias which papers a system learns to prioritize.

- **Prioritising References for Systematic Reviews with RobotAnalyst: A User Study**
  Przybyła, P., Brockmeier, A. J., Kontonatsios, G., et al., 2018, *Research Synthesis Methods*
  [Paper / DOI](https://doi.org/10.1002/jrsm.1311)
  Evaluates active-prioritization screening across 22 reference collections, showing large workload reduction alongside the need for stopping criteria.

- **Guidance on Terminology, Application, and Reporting of Citation Searching: The TARCiS Statement**
  Hirt, J., et al., 2024, *BMJ*
  [Paper / DOI](https://doi.org/10.1136/bmj-2023-078384)
  Methodological standard for reporting citation-searching practice, used in this repo's paper to argue for transparent retrieval provenance.

- **Citation Searching: A Systematic Review Case Study of Multiple Risk Behaviour Interventions**
  Wright, K., Golder, S., & Rodriguez-López, R., 2014, *BMC Medical Research Methodology*
  [Paper / DOI](https://doi.org/10.1186/1471-2288-14-73)
  Case study showing citation tracking across multiple databases recovers materially different result sets, demonstrating database-dependent coverage.

## Applications

- **Preliminary Evidence of Linguistic Bias in Academic Reviewing**
  Politzer-Ahles, S., Girolamo, T., & Ghali, S., 2020, *Journal of English for Academic Purposes*
  [Paper / DOI](https://doi.org/10.1016/j.jeap.2020.100895)
  Experimental evidence that less "native-like" academic English can lower quality ratings on otherwise-identical abstracts.

- **Publishing in English or Another Language: An Inclusive Study of Scholars' Language Publication Preferences**
  Stockemer, D., & Wigginton, M. J., 2019, *Scientometrics*
  [Paper / DOI](https://doi.org/10.1007/s11192-018-2987-0)
  Survey of 800+ authors finding non-Anglophone researchers publish the large majority of manuscripts in English, driven by perceived visibility gains.

- **Textual Analysis of Artificial Intelligence Manuscripts Reveals Features Associated with Peer Review Outcome**
  Vincent-Lamarre, P., & Larivière, V., 2021, *Quantitative Science Studies*
  [Paper / DOI](https://doi.org/10.1162/qss_a_00125)
  Analyzes 12,000+ AI manuscript submissions, finding linguistic and topical features correlated with acceptance and citation patterns.

## Evaluation Methods / Benchmarks

- **Google Scholar, Web of Science, and Scopus: A Systematic Comparison of Citations in 252 Subject Categories**
  Martín-Martín, A., Orduna-Malea, E., Thelwall, M., & Delgado López-Cózar, E., 2018, arXiv
  [Paper / DOI](https://arxiv.org/abs/1808.05053)
  Large-scale comparison of database coverage, showing Google Scholar captures substantial non-English and non-journal material absent from WoS/Scopus.

- **The Effect of English-Language Restriction on Systematic Review-Based Meta-Analyses**
  Morrison, A., Polisena, J., Husereau, D., et al., 2012, *International Journal of Technology Assessment in Health Care*
  [Paper / DOI](https://doi.org/10.1017/S0266462312000086)
  Systematic review finding language restriction doesn't always change pooled conclusions, but does reduce precision — evidence that language can't be assumed to be a safe proxy for relevance.

- **Conduct and Reporting of Citation Searching in Cochrane Systematic Reviews: A Cross-Sectional Study**
  Briscoe, S., Bethel, A., Rogers, M., et al., 2020, *Research Synthesis Methods*
  [Paper / DOI](https://doi.org/10.1002/jrsm.1355)
  Cross-sectional audit of how citation searching is actually conducted and reported in practice, exposing inconsistent methodology across reviews.

## Datasets

- **OpenAlex** — Open, comprehensive catalog of scholarly works, authors, venues, and citation links; used in this repo's paper as a source for automated citation-searching simulations. [openalex.org](https://openalex.org/)
- **Semantic Scholar Academic Graph (S2AG) / S2ORC** — Large open corpus of papers with full text, citation graphs, and embeddings, widely used for citation-recommendation and retrieval research. [api.semanticscholar.org](https://api.semanticscholar.org/)
- **CORE** — Aggregates open-access research outputs from repositories worldwide, including substantial non-English and regionally-indexed content useful for language-bias studies. [core.ac.uk](https://core.ac.uk/)

## Tools and Libraries

- **ASReview** — Open-source active-learning tool for systematic review screening; a practical example of a system where seed-label composition can shape which papers get prioritized. [asreview.ai](https://asreview.ai/)
- **OpenAlex API** — Programmatic access to works, citations, and concepts for building custom retrieval or citation-stratified sampling pipelines. [docs.openalex.org](https://docs.openalex.org/)
- **Semantic Scholar API** — REST API for paper search, citation graphs, and embeddings, usable for building popularity-blind or citation-stratified re-ranking experiments. [api.semanticscholar.org](https://api.semanticscholar.org/)
- **Connected Papers** — Visualizes citation networks as a graph, useful for inspecting whether citation-chaining seeds are producing a representative neighborhood. [connectedpapers.com](https://www.connectedpapers.com/)

## GitHub Implementations

- **asreview/asreview** — Source code for the ASReview active-learning screening tool referenced above. [github.com/asreview/asreview](https://github.com/asreview/asreview)
- **allenai/s2orc** — Tools and documentation for the Semantic Scholar Open Research Corpus. [github.com/allenai/s2orc](https://github.com/allenai/s2orc)
- **ourresearch/openalex-guts** — Backend/reference implementation details for the OpenAlex catalog. [github.com/ourresearch/openalex-guts](https://github.com/ourresearch/openalex-guts)

## Tutorials and Learning Resources

- **OpenAlex API Documentation** — Official guide to querying works, authors, and citation data. [docs.openalex.org](https://docs.openalex.org/)
- **Semantic Scholar API Documentation** — Official reference for paper search, citation, and recommendation endpoints. [api.semanticscholar.org/api-docs](https://api.semanticscholar.org/api-docs/)
- **ASReview Documentation** — Tutorials on setting up active-learning screening projects and interpreting active-learning behavior. [asreview.readthedocs.io](https://asreview.readthedocs.io/)
- **TARCiS Statement (Hirt et al., 2024)** — Practical guidance on terminology and reporting for citation searching, directly usable as a checklist. [doi.org/10.1136/bmj-2023-078384](https://doi.org/10.1136/bmj-2023-078384)

## License

This repository's original content (README, research paper, and citation integrity audit) is released under the MIT License unless otherwise noted. Linked third-party papers, datasets, and tools remain the property of their respective authors and publishers and are subject to their own licenses and terms of use.
