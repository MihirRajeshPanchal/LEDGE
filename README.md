# LEDGE : Leveraging Dependency Graphs for Enhanced Context Aware Documentation Generation
This repository contains code, datasets, visualizations, and analysis for the research project, *LEDGE : Leveraging Dependency Graphs for Enhanced Context Aware Documentation Generation*. a novel framework that integrates dependency graphs with large language models (LLMs) to automate the generation of structured, context aware software documentation

![architecture](https://github.com/user-attachments/assets/68d4864f-b4c2-40a9-b78d-1a0890c4063e)


## Folder Structure

```plaintext
├── README.md
├── LICENSE
├── datasets/
│   ├── average_evaluation_results.csv
│   ├── evaluation_results.csv
│   └── quantitative_analysis.csv
├── diagrams/
└── notebooks/
    ├── evaluation.ipynb
    └── graphs.ipynb
```

## Overview

### Project Objective

LEDGE addresses the problem of incomplete or outdated documentation in large codebases. It does so by:

* Constructing **dependency graphs** from source code using custom parsers.
* Storing these graphs in **MemGraph** using **Cypher queries** for fast retrieval.
* Embedding code symbols for **semantic similarity** matching.
* Using a **HybridRetriever** that combines graph traversal and vector search to provide the LLM with rich context.
* Generating accurate, structured documentation with **GraphRAG-based retrieval-augmented generation**.

---

### Dataset

We evaluated LEDGE on five diverse open-source repositories:

| Project   | URL                                                                        | Description                               |
| --------- | -------------------------------------------------------------------------- | ----------------------------------------- |
| Next.js   | [https://github.com/vercel/next.js](https://github.com/vercel/next.js)     | React framework for server-side rendering |
| MobX      | [https://github.com/mobxjs/mobx](https://github.com/mobxjs/mobx)           | State management library                  |
| Turborepo | [https://github.com/vercel/turborepo](https://github.com/vercel/turborepo) | Monorepo build system                     |
| Prisma    | [https://github.com/prisma/prisma](https://github.com/prisma/prisma)       | Type-safe database toolkit for TypeScript |
| Gatsby    | [https://github.com/gatsbyjs/gatsby](https://github.com/gatsbyjs/gatsby)   | React-based static site generator         |

LEDGE outperforms traditional documentation in both **qualitative** and **quantitative** evaluations using metrics like BLEU, ROUGE-L, BERTScore, and Jaccard similarity.

---

## Notebooks

The `notebooks/` folder includes interactive visualizations and reproducible analysis:

* [`evaluation.ipynb`](notebooks/evaluation.ipynb) — Analyzes BLEU, ROUGE, and BERTScore comparisons between LEDGE and baseline documentation.
* [`graphs.ipynb`](notebooks/graphs.ipynb) — Plots for research paper.

These notebooks replicate core results from the paper and demonstrate the impact of graph-based retrieval in documentation generation.

---

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for full details.

---

## Contact

For questions, collaborations, or feedback, feel free to reach out:

**Mihir Panchal** – [mihirpanchal5400@gmail.com](mailto:mihirpanchal5400@gmail.com) <br>
**Arnav Deo** – [arnav.nitin.deo@gmail.com](mailto:arnav.nitin.deo@gmail.com) <br>
**Varad Prabhu** – [varadprabhu111@gmail.com](mailto:varadprabhu111@gmail.com) <br>
**Prinkal Doshi** – [prinkaldoshi@gmail.com](mailto:prinkaldoshi@gmail.com) <br>
**Chetashri Bhadane** – [chetashri.bhadane@djsce.ac.in](mailto:chetashri.bhadane@djsce.ac.in) <br>
**Pranit Bari** – [pranit.bari@djsce.ac.in](mailto:pranit.bari@djsce.ac.in) <br>

