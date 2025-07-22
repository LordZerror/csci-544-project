# Knowledge Graphs Synthesis from Text: A Language Model Approach

This repository presents an automated pipeline for transforming unstructured domain-specific text into high-quality knowledge graphs using Large Language Models (LLMs), vector embeddings, and Retrieval-Augmented Generation (RAG).

The goal of this project is to automate the construction and evaluation of knowledge graphs (KGs) from research documents using:

- ✅ Overlapping context-preserving chunking
- ✅ SciBERT-based redundancy elimination
- ✅ Dual-mode triplet generation (Direct & RAG-based)
- ✅ LLM-as-a-Judge benchmarking framework

This approach addresses the limitations of previous KG pipelines by improving semantic coherence, reducing redundancy, and introducing a novel automated evaluation metric based on LLMs.

🧰 Features
1. 📄 Document Chunking: Splits text into overlapping 1,000-character snippets for context-rich triplet extraction.
2. 🔁 Redundancy Elimination: Uses SciBERT + Annoy vector similarity for deduplication.
3. 🔗 Triplet Generation:
  i. Direct Inference: LLM directly generates triplets from chunks.
  ii. RAG-based Inference: LLM retrieves context from full-text and generates richer relations.
4. 📊 LLM-Powered Evaluation: Gemini-2.0-Flash is used to score graphs on:
   i. Entity Coverage
   ii. Relation Clarity & Coherence
   iii. Graph Structure & Density
5. ⚙️ Incremental Updates: Vector DBs support real-time additions without re-indexing.

Results
1. Benchmarked Against: REBEL, iText2KG, AutoKG, and others
2. Best Performance: RAG-based Gemini model scored highest (7.63/10) across benchmarks
3. Improvements: Better contextual coverage, non-redundant relations, and deeper multi-hop insights

Kindly refer to the Final Report
