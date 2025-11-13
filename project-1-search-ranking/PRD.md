# Product Requirements Document (PRD)
## Project: Search Relevance Optimization  
## Author: Maureen Osauzo  
## Role: AI Product Manager  
## Portfolio Track: Perplexity APM

---

# 1. Overview

Users rely on search functionality to find accurate, contextually relevant answers.  
However, keyword-based search alone often leads to irrelevant or partially matching results.  
This project aims to improve **relevance ranking**, reduce friction, and help users find the *right information faster*.

This PRD outlines an end-to-end plan to evaluate and optimize search relevance using a hybrid approach:
- **BM25** (traditional lexical search)
- **Sentence Embeddings** (semantic search)

---

# 2. Problem Statement

Search results frequently return *technically correct* but *contextually irrelevant* answers.  
This leads to:
- Higher bounce rates  
- Poor user satisfaction  
- Increased cognitive load  
- Inconsistent ranking across query types  

Users need a search experience that understands **intent**, not just keywords.

---

# 3. Goals & Non-Goals

### Goals:
- Improve ranking quality for Q&A datasets  
- Minimize irrelevant results for ambiguous and complex queries  
- Compare BM25 vs embedding-based search  
- Build a prototype to visualize ranking differences  
- Establish a scalable evaluation framework (NDCG, Precision@k)  

### Non-Goals:
- Building a full production-grade search engine  
- Fine-tuning large language models  
- Complex UI or multi-language support  

---

# 4. User Personas

### Persona 1 — “The Quick Answer Seeker”
Motivation: Find accurate answers immediately  
Frustration: Clicking irrelevant results  

### Persona 2 — “The Deep Researcher”
Motivation: Needs contextually rich, multi-step answers  
Frustration: Shallow matches & keyword noise  

### Persona 3 — “The New User”
Motivation: Trust the system quickly  
Frustration: Confusing or poor early results damage trust  

---

# 5. User Stories

- “As a user, I want my top results to be relevant so I can get answers quickly.”  
- “As a researcher, I want the search engine to understand context so I don’t waste time.”  
- “As a new user, I want the search experience to feel intuitive and intelligent.”

---

# 6. Functional Requirements

- Users can input a query  
- System retrieves top-k documents (BM25 + Embeddings)  
- System displays ranking differences side-by-side  
- System displays relevance scores  
- Latency is displayed for each method  

---

# 7. Non-Functional Requirements

- Latency < 300ms  
- Runs in Replit without external GPU  
- Scalable for larger datasets if deployed  

---

# 8. Success Metrics

### Primary Metrics
- **NDCG@10**  
- **Precision@5**  
- **Mean Reciprocal Rank (MRR)**  
- **Latency (ms)**  

### Secondary Metrics
- Query intent match  
- Ambiguous query handling  
- Failure case reduction  

---

# 9. Technical Approach (Summary)

Implement a dual-system:
1. **BM25 (keyword-based)**
2. **Sentence Embeddings (semantic)**

Compare both methods across:
- Speed  
- Ranking quality  
- Query types  

---

# 10. Risks & Mitigations

### Risk: Semantic search may hallucinate matches.  
Mitigation: Showcase score + confidence & run BM25 for backup.

### Risk: Embedding models may bias toward long queries.  
Mitigation: Normalize scores.

### Risk: BM25 fails on synonyms.  
Mitigation: Use hybrid scoring for final recommendation.

---

# 11. Deliverables

- Replit prototype  
- Metrics dashboard  
- Comparison report  
- Architecture diagram  
- UX wireframes  
- GitHub documentation  

---

# 12. Timeline

Phase 1 — Data + Baseline (2 days)  
Phase 2 — BM25 vs Embedding evaluation (3 days)  
Phase 3 — Prototype + UX (2 days)  
Phase 4 — Documentation + Portfolio polish (1 day)  

---

# End of PRD
