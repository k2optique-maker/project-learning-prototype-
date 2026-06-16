# Semantic Data Governance Framework (PoC)

🎯 **Target Publication:** ISWC (International Semantic Web Conference) / ESWC - Posters and Demonstrations Track

## 📋 Research Abstract
In modern knowledge-intensive industries, organizing and re-using scattered explicit knowledge (such as siloed CSV data across departments) is essential for maximizing human creative productivity and fostering innovation. However, existing data governance approaches often suffer from data inconsistency and vocabulary misalignment. Furthermore, feeding unverified, fragmented data into black-box Large Language Models (LLMs) significantly increases the risk of hallucinations, hindering reliable "AI-ready" knowledge loops.

This repository explores lightweight semantic validation approaches using RDF and SHACL. While Ziegler (2020) conceptually discussed intelligent semantic content delivery (e.g., *microDocs*), the proposed framework provides a concrete, lightweight implementation protocol to bridge the gap between theory and execution. By transforming lightweight local CSV data into RDF graphs and applying W3C-standard **SHACL (Shapes Constraint Language)**, this framework aims to automatically detect lexical variations and semantic inconsistencies (focusing on L0→L1 detectability) at a minimal operational cost.

Crucially, while the scalable execution of this protocol naturally enables automation and the reduction of human labor within modern data pipelines, the primary objective of this prototype is to establish an explainable, governed foundation that secures a strict **Human-in-the-Loop (HITL)** architecture. By ensuring that the foundational semantic constraints and SHACL validation rules are firmly defined and governed by human experts, this framework prevents black-box autonomous rule alterations by AI as the system scales. This approach delivers a trusted, AI-ready data infrastructure that remains sustainable independent of changing AI vendor models, designed to scale seamlessly into DataOps pipelines, Change Data Capture (CDC), and Model Context Protocol (MCP).

*I am currently exploring these knowledge graphs and semantic technologies as part of my Master's research in Knowledge Science (JAIST), advancing step-by-step through agile implementation.*

