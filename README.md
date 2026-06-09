# Semantic Data Governance Framework (PoC)

**Target Publication:** ISWC (International Semantic Web Conference) / ESWC - Posters and Demonstrations Track

## About 
I am currently exploring knowledge graphs, semantic technologies, and "AI-ready" data governance as part of my interest in data-driven DX and reliable AI foundations. This repository serves as a concrete implementation protocol to verify how to model and validate real-world project data using a semantic approach.

## Problem 
In Large Language Model (LLM) environments and distributed data integration systems, data reliability and explainability are critically compromised when semantically inconsistent data (such as vocabulary mismatch or data silos) is used without being detected. Feeding unverified, fragmented explicit knowledge into black-box AI leads to higher risks of hallucinations.

## Goal
The goal of this Proof of Concept (PoC) is to establish a lightweight data governance layer using semantic constraints. By enabling the mechanical detection of data discrepancies and vocabulary variations, this framework verifies the minimum requirement for explainability and ensures that explicit knowledge is strictly "AI-ready."

## Scope
Targeting distributed, structured data where semantic consistency is not fully guaranteed, this study focuses on data detectability (L0→L1) within the broader concept of enterprise explainability. 

## Approach & Theoretical Foundation
While Ziegler (2020) conceptually discussed intelligent semantic content delivery (e.g., *microDocs*), the proposed framework provides a concrete, lightweight implementation protocol to bridge the gap between theory and execution. The protocol converts raw CSV data into RDF graphs and attempts to automatically detect lexical variations and semantic inconsistencies via SHACL constraints. 

This approach serves as a decentralized "building block" designed to scale into modern data engineering infrastructures such as DataOps pipelines, Change Data Capture (CDC), and Model Context Protocol (MCP).

## Research Origin & Evolution (Timeline)

The current "Minimal Semantic Refinement Protocol" is the result of a continuous, rigorous refactoring of the core research question, shifting from a conventional data integration mindset to a rigorous academic framework:

- **Phase 0-A: Initial Skepticism & Discovery (~6 Months Ago)**
  - Started with a fundamental question against the mainstream enterprise discourse: *"Does simply centralizing and integrating data truly unlock its value?"* 
  - This skepticism led to the discovery of Semantic Web technologies, where the initial goal was simply to verify how to construct a standard Knowledge Graph (KG) to solve data reuse problems.
- **Phase 0-B: Academic Refining & The Quest for Novelty (3 Months Ago)**
  - Upon entering the graduate research environment (JAIST), the focus shifted from mere system engineering ("just building a KG") to pursuing true academic novelty.
  - Deep-dive analysis revealed that feeding semantically inconsistent, fragmented explicit knowledge into black-box LLMs severely compromises explainability. The question evolved into: *"How can we mechanically govern distributed data to make it strictly AI-ready?"*
- **Phase 1: Arrival at the Minimal Protocol (Current / June 2026)**
  - Arrived at the definitive conclusion: A heavyweight, top-down ontology is unsustainable. The realistic, novel counter-offer is a lightweight, bottom-up approach: **"CSV ➡️ RDF ➡️ SHACL."**

## Progress & Milestones

### [Phase 1 Complete] RDF Graph Storage & Base Extraction Verification (June 2026)
- **Environment:** Successfully set up a local standalone server using **Apache Jena Fuseki (v5.6.0)**.
- **Data Injection:** Injected a 10-triple explicit knowledge dataset representing infrastructure project silos.
- **Results:** 
  - Validated basic retrieval via standard SPARQL queries, ensuring the environment is fully operational.
  - Visually confirmed "data fragmentation" (vocabulary mismatch) in the results, where conceptually identical nodes were split due to notation inconsistency. This perfectly demonstrated the real-world pain point of dead explicit knowledge.

## Next Steps
- **Phase 2:** Introduce the custom SHACL shape (`naming-shape.ttl`) to automatically detect these identity and structural inconsistencies under a strict constraint rule.

## Notes
This is an early-stage exploration for a Master's research project in Knowledge Science, advancing step-by-step through agile implementation.
