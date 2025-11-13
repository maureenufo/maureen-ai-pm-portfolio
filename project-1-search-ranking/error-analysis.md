# Error Analysis Report

## 1. Observed Failure Patterns

### BM25 Failures:
- Didn’t understand synonyms  
- Prioritized long documents  
- Returned irrelevant keyword matches  

### Embedding Failures:
- Occasionally returned semantically “close” but factually irrelevant results  
- Struggled with numeric queries  
- Biased toward generic content  

---

## 2. What These Failures Mean for Users

BM25 failures → Users get “technically matching but useless answers.”  
Embedding failures → Users get “contextually close but incorrect answers.”

Both can frustrate users for different reasons.

---

## 3. Recommendations

- Use embeddings as primary ranking for semantic queries  
- Use BM25 as backup for fact-heavy queries  
- Implement hybrid scoring weight: 0.7 embeddings / 0.3 BM25  
