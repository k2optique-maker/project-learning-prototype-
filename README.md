# Semantic Data Governance Framework (PoC)

🎯 **Target Publication:** ISWC (International Semantic Web Conference) / ESWC - Posters and Demonstrations Track

## 📋 Research Abstract
In modern knowledge-intensive industries, organizing and re-using scattered explicit knowledge (such as siloed CSV data across departments) is essential for maximizing human creative productivity and fostering innovation. However, existing data governance approaches often suffer from data inconsistency and vocabulary misalignment. Furthermore, feeding unverified, fragmented data into black-box Large Language Models (LLMs) significantly increases the risk of hallucinations, hindering reliable "AI-ready" knowledge loops.

To address these challenges as a realistic counter-offer to heavyweight, top-down enterprise solutions, this research proposes a bottom-up **"Minimal Semantic Refinement Protocol."** While Ziegler (2020) conceptually discussed intelligent semantic content delivery (e.g., *microDocs*), the proposed framework provides a concrete, lightweight implementation protocol to bridge the gap between theory and execution. By transforming lightweight local CSV data into RDF graphs and applying W3C-standard **SHACL (Shapes Constraint Language)**, this framework aims to automatically detect lexical variations and semantic inconsistencies (focusing on L0→L1 detectability) at a minimal operational cost.

Crucially, while the scalable execution of this protocol naturally enables automation and the reduction of human labor within modern data pipelines, the primary objective of this prototype is to establish an explainable, governed foundation that secures a strict **Human-in-the-Loop (HITL)** architecture. By ensuring that the foundational semantic constraints and SHACL validation rules are firmly defined and governed by human experts, this framework prevents black-box autonomous rule alterations by AI as the system scales. This approach delivers a trusted, AI-ready data infrastructure that remains sustainable independent of changing AI vendor models, designed to scale seamlessly into DataOps pipelines, Change Data Capture (CDC), and Model Context Protocol (MCP).

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

## 🚀 Next Steps & Evolutionary Roadmap

While the primary scope of this Master's research is strictly focused on establishing the core logic of the minimal protocol (**Phase 2**), the framework is conceptually engineered to scale into a multi-stage enterprise adoption process:

- **Phase 2 [Immediate]:** Introduce the custom SHACL shape (`naming-shape.ttl`) utilizing regular expressions (`sh:pattern`) to automatically detect identity and structural inconsistencies under a strict constraint rule.
- **Phase 3 [Agile Adoption Strategy - LPG Co-existence]:** Incorporate a lightweight **Labeled Property Graph (LPG)** layer (e.g., Neo4j/Memgraph) as an entry-level visualization tool. By utilizing LPG's schema-less nature to fast-track the "visual representation of fragmented data" (seeing is believing), this phase serves as an agile adoption hook to awaken organizational demand for data governance without demanding immediate top-down ontology compliance.
- **Phase 4 [Enterprise Scale & Cross-Border Evolution]:** Elevate the verified, high-purity data from the minimal protocol into a decentralized "building block" (Data Space) required for complex cross-border scenarios like M&A (PMI) and carve-outs. This tier natively scales into modern DataOps pipelines, Change Data Capture (CDC), and Model Context Protocol (MCP) to supply trusted, AI-ready assets to black-box LLMs.
