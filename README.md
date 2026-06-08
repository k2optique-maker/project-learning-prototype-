# project-learning-prototype-
This repository is a collection of my early-stage experiments and notes. I am currently exploring how to model real-world project data using a semantic approach.
# *Knowledge Graph / Semantic Web Learning Notes 

## About 
I am currently exploring knowledge graphs and semantic technologies as part of my interest in data-driven DX and AI foundations.

## Problem 
In LLMs and data integration environments, explainability is compromised when semantically inconsistent data is used without being detected.

## Goal
In this PoC, we will use semantic constraints to enable the detection of data discrepancies and verify the minimum requirements for explainability.

## Scope
Targeting structured data where semantic consistency is not fully guaranteed, this study focuses on detectability (L0→L1) within the broader concept of explainability.

## Approach
While Ziegler (2020) conceptually discussed semantic content delivery, our framework provides a concrete, lightweight implementation protocol using RDF/SHAC. We convert CSV data into RDF and attempt to detect lexical variations and semantic inconsistencies using SHACL constraints.

## 📈 Progress & Milestones

### 🟢 [Phase 1 Complete] RDF Graph Storage & Base Extraction Verification (June 2026)
- **Environment:** Successfully set up a local standalone server using **Apache Jena Fuseki (v5.6.0)**.
- **Data Injection:** Injected a 10-triple explicit knowledge dataset representing infrastructure project silos.
- **Results:** 
  - Validated basic retrieval via standard SPARQL queries, ensuring the environment is fully operational.
  - Visually confirmed "data fragmentation" (vocabulary mismatch) in the results, where conceptually identical nodes were split due to notation inconsistency. This perfectly demonstrated the real-world pain point of dead explicit knowledge.

## Next steps
- (Phase 2):** Introduce the custom SHACL shape (`naming-shape.ttl`) to automatically detect these identity inconsistencies under a strict constraint rule.

## Notes
This is still an early-stage exploration, and I'm learning as I go.



