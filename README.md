### Integrating Large Language Models for Enhanced Module Annotation  

**Authors:** Justin Seby¹, Ioannis Siavelis¹, Janne Lehtiö¹  
¹Cancer Proteomics Mass Spectrometry, Department of Oncology-Pathology, Karolinska Institutet  

---

## Overview  
Acute Myeloid Leukemia (AML) presents significant heterogeneity, challenging the interpretation of genetic alterations.  
We analyze a protein interaction network derived from **quantitative proteomics data** (12,241 proteins across 118 patients) using a **network-based framework enhanced with Large Language Models (LLMs)**.  

Our approach integrates machine learning, network biology, and LLM-powered annotation to enable **context-aware, scalable, and interpretable pathway insights** for cancer research.  

---

## Analytical Pipeline  
**1. Machine Learning Classifier**  
- Classifier combines traditional **distance features** with **GenePT embeddings** (literature-derived).  
- Positive pairs: sampled from CORUM.  
- Negative pairs: generated from CORUM non-complex proteins (100 sets, best representative selected).  
- Grid search: optimal 50:50 weighting → **Accuracy 82%, AUC 0.88**.  
- Model applied to score all protein pairs → **context-specific PPI network**.  

**2. PPI Network Construction & Validation**  
- **FDR control:** <0.01 (~95% confidence).  
- **Network size:** 8,459 proteins, 33,797 interactions.  
- **Scale-free topology:** verified via power-law distribution.  
- **Module detection:** Louvain clustering → 281 refined communities (size 5–100).  

**3. LLM Module Annotation**  
- GPT-4 & DeepSeek applied to annotate detected communities.  
- Benchmarked against enrichment-based annotations.  
- Showed **higher semantic specificity** and **confidence calibration** (e.g., HOX-driven hematopoiesis pathways).  

**4. Genetic Alteration Analysis**  
- Volcano plots highlight **SRSF2** and **NPM1** mutations.  
- BioGPT-powered **interactive chatbot** enables on-demand module annotation and reasoning.  

---

## Ongoing Work  
- **Explainable AI:** Add interpretability layers to chatbot outputs.  
- **Knowledge Integration:** PubMed RAG-based retrieval → build **biomedical knowledge base + structured graph**.  
- **User Interface:** Interactive portal for querying AML-specific networks and annotations.  

---

## References  
- Hu, M. et al. (2025). *Evaluation of large language models for discovery of gene set function.* **Nature Methods**, 22(1), 82–91. [https://doi.org/10.1038/s41592-024-02525-x](https://doi.org/10.1038/s41592-024-02525-x)  
- Chen, Y. & Zou, J. (2024). *GenePT: A simple but effective foundation model for genes and cells built from ChatGPT.* **bioRxiv**. [https://doi.org/10.1101/2023.10.16.562533](https://doi.org/10.1101/2023.10.16.562533)  

---

## Contact  
📧 **justin.seby@ki.se**  
🔗 [LinkedIn](https://linkedin.com/in/justinseby/)  

