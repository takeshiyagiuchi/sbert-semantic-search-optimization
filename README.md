# SBERT Semantic Search Optimization (Japanese)

This repository explores methods to improve **semantic similarity search performance** using SBERT models, with a focus on **Japanese text and location-based queries**.

The work covers the full pipeline, including dataset construction, model fine-tuning, representation improvements, evaluation, and inference optimization.

---

## Overview

Semantic similarity models often struggle with domain-specific inputs such as **location names**, especially in non-English settings.

This project focuses on:
- Improving similarity performance for **Japanese location names**
- Maintaining general semantic understanding using benchmark datasets
- Optimizing inference speed for practical deployment

All inputs and experiments are conducted in **Japanese**.

---

## Objectives

- Improve semantic similarity accuracy for location-related queries  
- Evaluate general performance using standard benchmarks  
- Explore representation-level improvements  
- Optimize inference latency and model efficiency  

---

## Methods

### 1. Data Collection
- Constructed custom datasets focused on **Japanese location names**  
- Generated additional datasets using structured sources (e.g., postal location lists)  
- Used **JSTS (Japanese STS Benchmark)** for general semantic similarity evaluation  

---

### 2. Fine-Tuning
- Fine-tuned SBERT models on domain-specific datasets  
- Compared performance before and after adaptation  

---

### 3. Representation Improvements

#### Vocabulary Expansion
- Explored extending token coverage for domain-specific terms  
- Evaluated impact on similarity performance  

#### Weighted Pooling
- Tested alternative pooling strategies beyond standard mean pooling  
- Aimed to better capture important tokens in location-based queries  

---

### 4. Evaluation

#### Semantic Similarity
- Evaluated using:
  - Pearson correlation  
  - Spearman correlation  
- Compared:
  - Domain-specific performance (location datasets)  
  - General performance (JSTS benchmark)  

---

### 5. Inference Optimization

#### Quantization
- Applied model quantization to reduce size and latency  
- Evaluated performance trade-offs  

#### CTranslate2
- Converted models for faster inference  
- Benchmarked latency improvements  

---

## Repository Structure

``` id="repo3"
sbert-semantic-search-optimization/
├── ctranslate2/                # Inference speed optimization with CTranslate2
├── datasets/                   # Custom datasets (location-based, JSTS reference)
├── fine-tuning/                # Fine-tuning experiments
├── inference_speed/            # Inference speed benchmarks
├── jppost/                     # Dataset generation using Japan Post location data
├── onnx/                       # Quantization experiments
├── pearson-spearman_scores/    # Semantic similarity evaluation
├── vocabulary_expansion/       # Vocabulary expansion experiments
├── weighted_pooling/           # Pooling strategy experiments
```

---

## Key Experiments

- Domain adaptation via fine-tuning on location datasets  
- Vocabulary expansion for improved token coverage  
- Weighted pooling for better sentence representation  
- Benchmark evaluation using JSTS  
- Inference acceleration using:
  - Quantization  
  - CTranslate2  

---

## Key Takeaways

- Domain-specific fine-tuning significantly improves similarity performance  
- Representation choices (pooling, vocabulary) impact results in subtle but meaningful ways  
- Inference optimization (quantization, CTranslate2) provides practical speed improvements with manageable trade-offs  

---

## Notes

- This repository is based on applied experiments and focuses on methodology and results  
- Some datasets are derived from publicly available sources (e.g., JSTS)  
- No proprietary or confidential data is included  

---