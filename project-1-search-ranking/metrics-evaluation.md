# Metrics & Evaluation

## 1. Ranking Metrics
### NDCG@10:
Measures overall ranking quality.

### Precision@k:
Measures how many returned results were actually relevant.

### MRR:
Measures how early the best answer appears.

---

## 2. Latency Metrics
- BM25 expected: < 100ms  
- Embeddings expected: 150–250ms  

---

## 3. Query Classes Tested
- Direct fact queries  
- Synonym-based queries  
- Ambiguous queries  
- Long-form context queries  

---

## 4. Results Summary (Example Template)

| Query Type        | BM25 NDCG | Embedding NDCG | Winner       |
|-------------------|-----------|----------------|--------------|
| Fact-based        | 0.81      | 0.78           | BM25         |
| Synonym-based     | 0.42      | 0.76           | Embeddings   |
| Ambiguous         | 0.51      | 0.67           | Embeddings   |
| Long-context      | 0.48      | 0.85           | Embeddings   |

