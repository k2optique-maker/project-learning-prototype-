# Semantic Data Governance Framework (PoC)

🎯 **Target Publication:** ISWC (International Semantic Web Conference) / ESWC - Posters and Demonstrations Track

## 📋 About 
I am currently exploring knowledge graphs, semantic technologies, and "AI-ready" data governance as part of my interest in data-driven DX and reliable AI foundations. This repository serves as a concrete implementation protocol to verify how to model and validate real-world project data using a semantic approach.

## ⚠️ Problem 
In Large Language Model (LLM) environments and distributed data integration systems, data reliability and explainability are critically compromised when semantically inconsistent data (such as vocabulary mismatch or data silos) is used without being detected. Feeding unverified, fragmented explicit knowledge into black-box AI leads to higher risks of hallucinations.

## 🎯 Goal
The goal of this Proof of Concept (PoC) is to establish a lightweight data governance layer using semantic constraints. By enabling the mechanical detection of data discrepancies and vocabulary variations, this framework verifies the minimum requirement for explainability and ensures that explicit knowledge is strictly "AI-ready."

## 🔍 Scope
Targeting distributed, structured data where semantic consistency is not fully guaranteed, this study focuses on data detectability (L0→L1) within the broader concept of enterprise explainability. 

## 💡 Approach & Theoretical Foundation
While Ziegler (2020) conceptually discussed intelligent semantic content delivery (e.g., *microDocs*), this framework provides a concrete, lightweight implementation protocol using W3C standards (RDF/SHACL) to bridge the gap between theory and execution. We convert raw CSV data into RDF graphs and attempt to detect lexical variations and semantic inconsistencies automatically via SHACL constraints. 

This approach serves as a decentralized "building block" designed to scale into modern data engineering infrastructures such as DataOps pipelines, Change Data Capture (CDC), and Model Context Protocol (MCP).

## 📈 Progress & Milestones

### 🟢 [Phase 1 Complete] RDF Graph Storage & Base Extraction Verification (June 2026)
- **Environment:** Successfully set up a local standalone server using **Apache Jena Fuseki (v5.6.0)**.
- **Data Injection:** Injected a 10-triple explicit knowledge dataset representing infrastructure project silos.
- **Results:** 
  - Validated basic retrieval via standard SPARQL queries, ensuring the environment is fully operational.
  - Visually confirmed "data fragmentation" (vocabulary mismatch) in the results, where conceptually identical nodes were split due to notation inconsistency. This perfectly demonstrated the real-world pain point of dead explicit knowledge.

## 🚀 Next Steps
- **Phase 2:** Introduce the custom SHACL shape (`naming-shape.ttl`) to automatically detect these identity and structural inconsistencies under a strict constraint rule.

## 📝 Notes
This is an early-stage exploration for a Master's research project in Knowledge Science, advancing step-by-step through agile implementation.
