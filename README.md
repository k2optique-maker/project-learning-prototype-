# Semantic Data Governance Framework (PoC)

🎯 **Target Publication:** ISWC (International Semantic Web Conference) / ESWC - Posters and Demonstrations Track

## 📋 Research Abstract
In modern knowledge-intensive industries, organizing and re-using scattered explicit knowledge (such as siloed CSV data across departments) is essential for maximizing human creative productivity and fostering innovation. However, existing data governance approaches often suffer from data inconsistency and vocabulary misalignment. Furthermore, feeding unverified, fragmented data into black-box Large Language Models (LLMs) significantly increases the risk of hallucinations, hindering reliable "AI-ready" knowledge loops.

To address these challenges as a realistic counter-offer to heavyweight, top-down enterprise solutions, this research proposes a bottom-up **"Minimal Semantic Refinement Protocol."** While Ziegler (2020) conceptually discussed intelligent semantic content delivery (e.g., *microDocs*), the proposed framework provides a concrete, lightweight implementation protocol to bridge the gap between theory and execution. By transforming lightweight local CSV data into RDF graphs and applying W3C-standard **SHACL (Shapes Constraint Language)**, this framework aims to automatically detect lexical variations and semantic inconsistencies (focusing on L0→L1 detectability) at a minimal operational cost.

The primary objective of this prototype is not merely technical implementation, but to establish an explainable, governed data foundation that secures a safety net for human-AI co-creation. This decentralized "building block" ensures sustainable knowledge assets independent of changing AI vendor models, designed to scale into modern DataOps pipelines, Change Data Capture (CDC), and Model Context Protocol (MCP).

*I am currently exploring these knowledge graphs and semantic technologies as part of my Master's research in Knowledge Science (JAIST), advancing step-by-step through agile implementation.*

## 📜 Research Origin & Evolution (Timeline)
The current protocol is the result of a continuous, rigorous refactoring of the core research question, shifting from a conventional data integration mindset to an academic framework:

- **Phase 0-A: Initial Skepticism & Discovery (~6 Months Ago)**
  - Started with a fundamental question against mainstream DX discourse: *"Does simply centralizing and integrating data truly unlock its value?"* 
  - This skepticism led to the discovery of Semantic Web technologies, where the initial goal was simply to verify how to construct a standard Knowledge Graph (KG) to solve data reuse problems.
- **Phase 0-B: Academic Refining & The Quest for Novelty (3 Months Ago)**
  - Upon entering the graduate environment, the focus shifted from mere system engineering to pursuing true academic novelty.
  - Deep-dive analysis revealed that feeding semantically inconsistent data into black-box LLMs severely compromises explainability. The question evolved into: *"How can we mechanically govern distributed data to make it strictly AI-ready?"*
- **Phase 1: Arrival at the Minimal Protocol (Current / June 2026)**
  - Arrived at the definitive conclusion: A heavyweight, top-down ontology is unsustainable. The realistic, novel counter-offer is a lightweight, bottom-up approach: **"CSV ➡️ RDF ➡️ SHACL."**

## 📈 Progress & Milestones

### 🟢 [Phase 1 Complete] RDF Graph Storage & Base Extraction Verification (June 2026)
- **Environment:** Successfully set up a local standalone server using **Apache Jena Fuseki (v5.6.0)**.
- **Data Injection:** Injected a 10-triple explicit knowledge dataset representing infrastructure project silos.
- **Results:** 
  - Validated basic retrieval via standard SPARQL queries, ensuring the environment is fully operational.
  - Visually confirmed "data fragmentation" (vocabulary mismatch) in the results, where conceptually identical nodes were split due to notation inconsistency. This perfectly demonstrated the real-world pain point of dead explicit knowledge.

## 🚀 Next Steps
- **Phase 2:** Introduce the custom SHACL shape (`naming-shape.ttl`) utilizing regular expressions (`sh:pattern`) to automatically detect these identity and structural inconsistencies under a strict constraint rule.
