# Awesome AI Literature Curation Bias

A curated collection of research papers, datasets, tools, implementations, and learning resources related to **recall bias toward highly-cited and English-language papers in AI literature curation**.

This repository is based on the same topic used in my AI-assisted research paper and citation-integrity audit. It brings together research and practical resources related to citation bias, language bias, scholarly search and recommendation, automated literature screening, and AI-assisted research discovery.

## Contents

* [Topic Overview](#topic-overview)
* [AI-Assisted Research Paper](#ai-assisted-research-paper)
* [Citation Integrity Audit](#citation-integrity-audit)
* [Survey and Review Papers](#survey-and-review-papers)
* [Foundational Papers](#foundational-papers)
* [Recent Research Papers](#recent-research-papers)
* [Methods and Algorithms](#methods-and-algorithms)
* [Applications](#applications)
* [Evaluation Methods and Benchmarks](#evaluation-methods-and-benchmarks)
* [Datasets](#datasets)
* [Tools and Libraries](#tools-and-libraries)
* [GitHub Implementations](#github-implementations)
* [Tutorials and Learning Resources](#tutorials-and-learning-resources)
* [License](#license)

## Topic Overview

AI-based systems are increasingly being used to find, rank, recommend, and screen research papers. Search engines, citation networks, scholarly recommendation systems, and large language models can make literature discovery much faster, but the way these systems select and rank papers can affect which research becomes visible.

This repository focuses on **recall bias in AI literature curation**, particularly the possibility that highly-cited papers and papers published in English receive greater visibility than relevant papers with fewer citations or papers published in other languages.

Citation counts are not always a direct measure of research quality. Citation patterns can be affected by factors such as popularity, previous recognition, publication venue, language, and accessibility. Similarly, literature databases and retrieval systems may differ in their coverage of papers from different languages and sources.

The research collected here covers these issues from several perspectives, including citation bias, cumulative advantage, scholarly recommender systems, language and publishing bias, citation searching, automated screening, retrieval evaluation, and AI-assisted literature reviews.

The aim of this repository is to provide a useful starting point for understanding the problem and for finding datasets, tools, implementations, and research methods that can be used to study it.

## AI-Assisted Research Paper

### Recall Bias Toward Highly-Cited and English-Language Papers in AI Literature Curation

This is the original AI-assisted research paper prepared for the assigned research topic.

The paper discusses recall bias in literature curation and connects it with citation bias, cumulative advantage, language bias, bibliographic database coverage, scholarly recommender systems, citation searching, and automated literature screening.

[View the AI-Assisted Research Paper](paper/AI_Assisted_Research_Paper.pdf)

## Citation Integrity Audit

The references in the AI-generated research paper were checked as part of the **AI-Assisted Citation Integrity Audit**.

The original paper contained **23 references**. Following the laboratory sampling procedure, 10 references were selected for detailed verification.

The audit checked whether the publications existed and whether their titles, authors, publication years, venues, and identifiers matched the scholarly records.

### Audit Results

| Classification          | Number |
| ----------------------- | -----: |
| A — Verified            |      8 |
| B — Wrong Metadata      |      2 |
| C — Frankenstein        |      0 |
| D — Fabricated          |      0 |
| E — Identifier Mismatch |      0 |
| **Total Audited**       | **10** |

The resulting **Authenticity Score was 95/100**, and the **Prediction Accuracy was 70%**.

The audit showed that a citation can appear genuine and still contain incorrect bibliographic information. Two of the audited references were genuine publications but had an incorrect publication year in the AI-generated reference.

[View Citation Integrity Audit](citation-audit/Citation_Integrity_Audit.pdf)

## Survey and Review Papers

This section contains review and survey papers that provide background on citation recommendation, scholarly recommender systems, popularity bias, and citation patterns.

* **Biases in Scholarly Recommender Systems: Impact, Prevalence, and Mitigation**
  Färber, M., Coutinho, M., & Yuan, S., 2023, *Scientometrics*.
  [Paper / DOI](https://doi.org/10.1007/s11192-023-04636-2)
  Reviews different forms of bias in scholarly recommender systems, including popularity and selection effects.

* **Citation Recommendation: Approaches and Datasets**
  Färber, M. & Jatowt, A., 2020, *International Journal on Digital Libraries*.
  [Paper / DOI](https://doi.org/10.1007/s00799-020-00288-2)
  Surveys citation recommendation approaches and the datasets used to develop them.

* **A Survey on Popularity Bias in Recommender Systems**
  Klimashevskaia, A., Jannach, D., Elahi, M., & Trattner, C., 2024, *User Modeling and User-Adapted Interaction*.
  [Paper / DOI](https://doi.org/10.1007/s11257-024-09406-0)
  Provides background on popularity bias and the tendency of recommendation systems to favor already-popular items.

* **Predictors of Citation Rates and the Problem of Citation Bias: A Scoping Review**
  Lund, H., et al., 2025, *Journal of Clinical Epidemiology*.
  [Paper / DOI](https://doi.org/10.1016/j.jclinepi.2025.112057)
  Examines factors associated with citation rates and the problem of treating citations as a simple measure of research quality.

## Foundational Papers

* **The Matthew Effect in Science**
  Merton, R. K., 1968, *Science*.
  [Paper / DOI](https://doi.org/10.1126/science.159.3810.56)
  Introduces the Matthew effect and the idea of cumulative advantage in scientific recognition.

* **The Matthew Effect in Science, II: Cumulative Advantage and the Symbolism of Intellectual Property**
  Merton, R. K., 1988, *Isis*.
  [Paper / DOI](https://doi.org/10.1086/354848)
  Further develops the concept of cumulative advantage in science.

* **Collaborative Topic Modeling for Recommending Scientific Articles**
  Wang, C. & Blei, D. M., 2011, ACM SIGKDD.
  [Paper / DOI](https://doi.org/10.1145/2020408.2020480)
  Provides a foundation for recommendation of scientific articles using topic information.

* **Introduction: Hegemonic Languages and Science**
  Gordin, M. D., 2017, *Isis*.
  [Paper / DOI](https://doi.org/10.1086/694164)
  Discusses the historical development of English as a dominant language in international science.

* **Scientific Citations Favor Positive Results: A Systematic Review and Meta-Analysis**
  Duyx, B., Urlings, M. J. E., Swaen, G. M. H., Bouter, L. M., & Zeegers, M. P., 2017, *Journal of Clinical Epidemiology*.
  [Paper / DOI](https://doi.org/10.1016/j.jclinepi.2017.06.002)
  Examines evidence that positive research findings receive more citations.

## Recent Research Papers

* **Comparing Supervised Machine Learning and Large Language Models in Title-Abstract Screening**
  Aigner, M. F., Ganzinger, M., Probst, P., Rinckens, M., & Pausch, T. M., 2026, *Systematic Reviews*.
  [Paper / DOI](https://doi.org/10.1186/s13643-026-03199-6)
  Compares machine-learning and large-language-model approaches for title and abstract screening.

* **The Use of Generative Artificial Intelligence in Systematic Literature Reviews: A Rapid Review**
  Fleurence, R. L., Qureshi, R., Aggarwal, R., et al., 2026, *Value in Health*.
  [Paper / DOI](https://doi.org/10.1016/j.jval.2026.06.012)
  Reviews the use of generative AI in different stages of systematic literature reviews.

* **Automated Citation Searching in Systematic Review Production: A Simulation Study**
  Rajit, D., Du, L., Teede, H., & Enticott, J., 2025, *Research Synthesis Methods*.
  [Paper / DOI](https://doi.org/10.1017/rsm.2024.15)
  Investigates automated citation searching and compares its retrieval characteristics with manual searching.

## Methods and Algorithms

* **ASReview: Active Learning for Systematic Reviews**
  Van de Schoot, R., de Bruin, J., Schram, R., et al., 2021.
  [Paper / DOI](https://doi.org/10.5281/zenodo.5126631)
  Provides an active-learning approach for prioritizing references during systematic review screening.

* **Prioritising References for Systematic Reviews with RobotAnalyst: A User Study**
  Przybyła, P., Brockmeier, A. J., Kontonatsios, G., et al., 2018, *Research Synthesis Methods*.
  [Paper / DOI](https://doi.org/10.1002/jrsm.1311)
  Studies automated prioritization of references to reduce screening workload.

* **Guidance on Terminology, Application, and Reporting of Citation Searching: The TARCiS Statement**
  Hirt, J., et al., 2024, *BMJ*.
  [Paper / DOI](https://doi.org/10.1136/bmj-2023-078384)
  Provides guidance for conducting and reporting citation searching.

* **Citation Searching: A Systematic Review Case Study of Multiple Risk Behaviour Interventions**
  Wright, K., Golder, S., & Rodriguez-López, R., 2014, *BMC Medical Research Methodology*.
  [Paper / DOI](https://doi.org/10.1186/1471-2288-14-73)
  Shows how citation searching can produce additional and different literature from database searching.

## Applications

* **Preliminary Evidence of Linguistic Bias in Academic Reviewing**
  Politzer-Ahles, S., Girolamo, T., & Ghali, S., 2020, *Journal of English for Academic Purposes*.
  [Paper / DOI](https://doi.org/10.1016/j.jeap.2020.100895)
  Investigates the effect of linguistic features on academic evaluation.

* **Publishing in English or Another Language: An Inclusive Study of Scholars' Language Publication Preferences**
  Stockemer, D. & Wigginton, M. J., 2019, *Scientometrics*.
  [Paper / DOI](https://doi.org/10.1007/s11192-018-2987-0)
  Examines researchers' publication-language preferences and the perceived visibility advantages of English.

* **Textual Analysis of Artificial Intelligence Manuscripts Reveals Features Associated with Peer Review Outcome**
  Vincent-Lamarre, P. & Larivière, V., 2021, *Quantitative Science Studies*.
  [Paper / DOI](https://doi.org/10.1162/qss_a_00125)
  Studies textual characteristics of AI manuscripts and their relationship with peer-review outcomes.

## Evaluation Methods and Benchmarks

* **Google Scholar, Web of Science, and Scopus: A Systematic Comparison of Citations in 252 Subject Categories**
  Martín-Martín, A., Orduna-Malea, E., Thelwall, M., & Delgado López-Cózar, E., 2018.
  [Paper](https://arxiv.org/abs/1808.05053)
  Compares major scholarly databases and their coverage of research publications and citations.

* **The Effect of English-Language Restriction on Systematic Review-Based Meta-Analyses**
  Morrison, A., Polisena, J., Husereau, D., et al., 2012, *International Journal of Technology Assessment in Health Care*.
  [Paper / DOI](https://doi.org/10.1017/S0266462312000086)
  Examines the effect of restricting systematic reviews to English-language studies.

* **Conduct and Reporting of Citation Searching in Cochrane Systematic Reviews: A Cross-Sectional Study**
  Briscoe, S., Bethel, A., Rogers, M., et al., 2020, *Research Synthesis Methods*.
  [Paper / DOI](https://doi.org/10.1002/jrsm.1355)
  Examines how citation searching is conducted and reported in systematic reviews.

## Datasets

The datasets used in this repository are sources that can provide scholarly metadata, papers, or citation information relevant to studying literature discovery and citation patterns.

* **OpenAlex** — An open scholarly data source containing works, authors, venues, concepts, and citation relationships. It can be used for analysing citation patterns and constructing literature datasets.
  [OpenAlex](https://openalex.org/)

* **Semantic Scholar Academic Graph / S2ORC** — Provides scholarly information including papers, references, citations, and related research data. It is useful for citation-network and literature-retrieval research.
  [Semantic Scholar](https://www.semanticscholar.org/)

* **CORE** — A large collection of open-access research outputs gathered from repositories and other sources. Its broad coverage can be useful when studying research visibility and literature retrieval.
  [CORE](https://core.ac.uk/)

[More details about the datasets](datasets/datasets.md)

## Tools and Libraries

* **ASReview** — An open-source tool for active-learning based literature screening. It is useful for studying automated prioritization during systematic reviews.
  [ASReview](https://asreview.ai/)

* **OpenAlex API** — Provides programmatic access to scholarly works, authors, concepts, and citation information.
  [OpenAlex API Documentation](https://docs.openalex.org/)

* **Semantic Scholar API** — Provides access to scholarly papers, citations, authors, and related information for literature-retrieval applications.
  [Semantic Scholar API](https://api.semanticscholar.org/)

* **Connected Papers** — A visual tool for exploring relationships between research papers and related literature.
  [Connected Papers](https://www.connectedpapers.com/)

[More details about the tools](tools/tools.md)

## GitHub Implementations

The following open-source projects provide implementations or resources related to literature screening, scholarly data, and citation-based research.

* **asreview/asreview** — Source code for the ASReview active-learning screening system.
  [GitHub Repository](https://github.com/asreview/asreview)

* **allenai/s2orc** — Resources and tools associated with the Semantic Scholar Open Research Corpus.
  [GitHub Repository](https://github.com/allenai/s2orc)

* **ourresearch/openalex-guts** — Open-source components associated with the OpenAlex scholarly-data infrastructure.
  [GitHub Repository](https://github.com/ourresearch/openalex-guts)

[More details about the implementations](implementations/github-repositories.md)

## Tutorials and Learning Resources

* **OpenAlex API Documentation** — Documentation for querying scholarly works, authors, concepts, and citation information.
  [OpenAlex Documentation](https://docs.openalex.org/)

* **Semantic Scholar API Documentation** — Documentation for accessing papers and citation information through the Semantic Scholar API.
  [Semantic Scholar API Documentation](https://api.semanticscholar.org/api-docs/)

* **ASReview Documentation** — Documentation and tutorials for using active learning in systematic literature screening.
  [ASReview Documentation](https://asreview.readthedocs.io/)

* **TARCiS Statement** — Guidance for citation searching terminology, application, and reporting.
  [TARCiS / BMJ](https://doi.org/10.1136/bmj-2023-078384)

* **Semantic Scholar** — Scholarly search and discovery platform that can be used to explore papers, citations, and related research.
  [Semantic Scholar](https://www.semanticscholar.org/)

## Repository Structure

```text
awesome-ai-literature-recall-bias/
│
├── README.md
├── LICENSE
│
├── paper/
│   └── Recall Bias Toward Highly-Cited and English-Language Papers in AI Literature Curation.pdf
│
├── citation-audit/
│   └── Citation_Integrity_Audit.pdf
│
├── references/
│   └── references.md
│
├── datasets/
│   └── datasets.md
│
├── tools/
│   └── tools.md
│
└── implementations/
    └── github-repositories.md
```

## License

This repository's original content is released under the MIT License unless otherwise stated.

The research papers, datasets, tools, and external repositories linked here belong to their respective authors or organizations and are subject to their own licenses and terms of use.
