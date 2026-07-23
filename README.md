````markdown
# Model-Driven Quantum Code Generation Using LLMs and RAG

This repository contains the source code and experimental results for generating executable quantum code from Unified Modeling Language (UML) model instances using Large Language Models (LLMs) and Retrieval-Augmented Generation (RAG).

The approach uses GPT-4o to generate Python code compatible with IBM’s [Qiskit](https://www.ibm.com/quantum/qiskit) library. It evaluates how prompt specificity and RAG-based contextual information affect the correctness, completeness, and structural similarity of the generated quantum code. :contentReference[oaicite:0]{index=0}

---

## Repository Structure

```text
QuantumCodeGeneration/
├── Quantum Code Generation/
│   ├── Notebooks/
│   │   ├── C1/                         # Notebooks for model instance 1
│   │   ├── C2/                         # Notebooks for model instance 2
│   │   ├── C3/                         # Notebooks for model instance 3
│   │   ├── C4/                         # Notebooks for model instance 4
│   │   ├── C5/                         # Notebooks for model instance 5
│   │   ├── C6/                         # Notebooks for model instance 6
│   │   └── C7/                         # Notebooks for model instance 7
│   │
│   └── Evaluation Results/
│       ├── C1/                         # Generated code and results for C1
│       ├── C2/                         # Generated code and results for C2
│       ├── C3/                         # Generated code and results for C3
│       ├── C4/                         # Generated code and results for C4
│       ├── C5/                         # Generated code and results for C5
│       ├── C6/                         # Generated code and results for C6
│       └── C7/                         # Generated code and results for C7
│
├── LICENSE
└── README.md
````

Each case-study directory contains notebooks and results for four experimental configurations:

* Generic prompt without RAG
* Generic prompt with RAG
* Specific prompt without RAG
* Specific prompt with RAG

---

## Approach

The input to the code-generation pipeline is a textual UML model instance describing a classical-quantum software system. The LLM generates Python code that implements the corresponding quantum circuit using Qiskit.

The RAG configuration retrieves relevant Qiskit code from public GitHub repositories and provides the retrieved content as additional context to the LLM.

The experiments investigate:

1. Whether an LLM can generate quantum code from UML model instances.
2. Whether RAG improves the generated code.
3. Whether detailed prompt engineering improves generation quality.

---

## Experimental Cases

The experiments use seven UML model instances, represented in the repository as `C1` through `C7`. Each model instance is evaluated under all four prompt and RAG configurations.

The notebooks generate:

* Qiskit-compatible Python code
* Element-level evaluation reports
* Quantum and non-quantum evaluation results
* Spreadsheet outputs used to calculate the reported metrics

---

## Evaluation Metrics

The generated code is evaluated using:

| Metric      | Description                                              |
| ----------- | -------------------------------------------------------- |
| Precision   | Correctness of the generated elements                    |
| Recall      | Completeness of the generated elements                   |
| F-measure   | Harmonic mean of Precision and Recall                    |
| Q-Precision | Precision for quantum gates and quantum partitions       |
| Q-Recall    | Recall for quantum gates and quantum partitions          |
| Q-F-measure | F-measure for quantum-specific elements                  |
| CodeBLEU    | Structural and semantic similarity to the reference code |

---

## Key Results

The experiments show that prompt engineering has a greater effect on code-generation quality than the RAG configuration used in this study.

For model instance 1, replacing the generic prompt with the specific prompt increased the average CodeBLEU score from **0.16 to 0.57** without RAG. 

The current RAG configuration produced only limited improvements, suggesting that more relevant and structured retrieval sources may be required.

---

## Paper

This repository supports the following paper:

> **N. Siavash and A. Moin, “Model-Driven Quantum Code Generation Using Large Language Models and Retrieval-Augmented Generation,”**
> *2025 ACM/IEEE 28th International Conference on Model Driven Engineering Languages and Systems (MODELS)*, Grand Rapids, MI, USA, 2025, pp. 260–266.
> DOI: [10.1109/MODELS67397.2025.00031](https://doi.org/10.1109/MODELS67397.2025.00031)

### Citation

```bibtex
@inproceedings{siavash2025model,
  author    = {Nazanin Siavash and Armin Moin},
  title     = {Model-Driven Quantum Code Generation Using Large Language Models and Retrieval-Augmented Generation},
  booktitle = {2025 ACM/IEEE 28th International Conference on Model Driven Engineering Languages and Systems (MODELS)},
  year      = {2025},
  pages     = {260--266},
  doi       = {10.1109/MODELS67397.2025.00031}
}
```

---

## Keywords

Model-driven software engineering, quantum code generation, quantum computing, large language models, LLMs, retrieval-augmented generation, RAG, UML, Qiskit, Python, prompt engineering, and software engineering.

---

## License

This project is licensed under the terms of the `LICENSE` file included in this repository.

---

## Acknowledgments

This work was funded by a grant from the Colorado Office of Economic Development and International Trade (OEDIT).

```
```
