# Quantum Code Generation
This project introduces a novel research direction for model-to-text/code transformations by leveraging Large Language Models (LLMs) that can be enhanced with Retrieval-Augmented Generation (RAG) pipelines. The focus is on quantum and hybrid quantum-classical software systems, where model-driven approaches can help reduce the costs and mitigate the risks associated with the heterogeneous platform landscape and lack of developers’ skills. We validate one of the proposed ideas regarding generating code out of UML model instances of software systems. This Python code uses a well-established library, called Qiskit, to execute on gate-based or circuit-based quantum computers. The RAG pipeline that we deploy incorporates sample Qiskit code from public GitHub repositories. Experimental results show that well-engineered prompts can improve CodeBLEU scores by up to a factor of four, yielding more accurate and consistent quantum code. However, the proposed research direction can go beyond this through further investigation in the future by conducting experiments to address our other research questions and ideas proposed here, such as deploying software system model instances as the source of information in the RAG pipelines, or deploying LLMs for code-to-code transformations, for instance, for transpilation use cases.

## Paper

This repository contains the source code and resources associated with the following paper:

> N. Siavash and A. Moin, “Model-Driven Quantum Code Generation Using Large Language Models and Retrieval-Augmented Generation,” in *Proceedings of the 2025 ACM/IEEE 28th International Conference on Model Driven Engineering Languages and Systems (MODELS)*, Grand Rapids, MI, USA, 2025, pp. 260–266. DOI: [10.1109/MODELS67397.2025.00031](https://doi.org/10.1109/MODELS67397.2025.00031).

### Keywords

Model-driven software engineering, quantum code generation, quantum computing, large language models, LLMs, retrieval-augmented generation, RAG, Unified Modeling Language, software engineering, and Python.
