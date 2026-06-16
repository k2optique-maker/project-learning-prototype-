# Semantic Data Governance Framework (PoC)

🎯 **Target Publication:** ISWC (International Semantic Web Conference) / ESWC - Posters and Demonstrations Track

## 📋 Research Abstract
In modern knowledge-intensive industries, organizing and re-using scattered explicit knowledge (such as siloed CSV data across departments) is essential for maximizing human creative productivity and fostering innovation. However, existing data governance approaches often suffer from data inconsistency and vocabulary misalignment. Furthermore, feeding unverified, fragmented data into black-box Large Language Models (LLMs) significantly increases the risk of hallucinations, hindering reliable "AI-ready" knowledge loops.

This repository explores lightweight semantic validation approaches using RDF and SHACL. While Ziegler (2020) conceptually discussed intelligent semantic content delivery (e.g., *microDocs*), the proposed framework provides a concrete, lightweight implementation protocol to bridge the gap between theory and execution. By transforming lightweight local CSV data into RDF graphs and applying W3C-standard **SHACL (Shapes Constraint Language)**, this framework aims to automatically detect lexical variations and semantic inconsistencies (focusing on L0→L1 detectability) at a minimal operational cost.

Crucially, while the scalable execution of this protocol naturally enables automation and the reduction of human labor within modern data pipelines, the primary objective of this prototype is to establish an explainable, governed foundation that secures a strict **Human-in-the-Loop (HITL)** architecture. By ensuring that the foundational semantic constraints and SHACL validation rules are firmly defined and governed by human experts, this framework prevents black-box autonomous rule alterations by AI as the system scales. This approach delivers a trusted, AI-ready data infrastructure that remains sustainable independent of changing AI vendor models, designed to scale seamlessly into DataOps pipelines, Change Data Capture (CDC), and Model Context Protocol (MCP).

*I am currently exploring these knowledge graphs and semantic technologies as part of my Master's research in Knowledge Science (JAIST), advancing step-by-step through agile implementation.*



## 📈 Progress & Milestones

### 🟢 [Phase 1 Complete] RDF Graph Storage & Base Extraction Verification (June 2026)
- **Environment:** Successfully set up a local standalone server using **Apache Jena Fuseki (v5.6.0)**.
- **Data Injection:** Injected a 10-triple explicit knowledge dataset representing infrastructure project silos.
- **Results:** 
  - Validated basic retrieval via standard SPARQL queries, ensuring the environment is fully operational.
  - Visually confirmed "data fragmentation" (vocabulary mismatch) in the results, where conceptually identical nodes were split due to notation inconsistency. This perfectly demonstrated the real-world pain point of dead explicit knowledge.

## 🚀 Next Steps & Evolutionary Roadmap

While the primary scope of this Master's research is strictly limited to verifying the core validation logic of the minimal protocol (**Phase 2**), the framework conceptually designs a multi-stage enterprise adoption model to ensure usability:

- **Phase 2 [Immediate / Current Scope]:** Introduce the custom SHACL shape (`naming-shape.ttl`) utilizing regular expressions (`sh:pattern`) to automatically detect identity and structural inconsistencies. *This research focuses entirely on this phase to secure academic rigor within the Master's timeline.*
- **Future Work [Conceptual Adoption Strategy - LPG Integration]:** Propose a hybrid transition roadmap where a lightweight **Labeled Property Graph (LPG)** layer (e.g., Neo4j/Memgraph) can be deployed prior to RDF conversion. Utilizing LPG's schema-less nature functions as a visual adoption hook (seeing is believing) to awaken organizational demand for data governance, enhancing the long-term usability and scalability into DataOps pipelines without increasing immediate implementation overhead.

