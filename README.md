
<img src="https://github.com/lbj2011/PV-LLM/blob/main/doc_img/LLM%20LOGO.jpg" width="300"/>

# PV-LLM: Leveraging Multimodal LLMs for PV Analysis

PV-LLM is a novel framework that utilizes **multimodal large language models (LLMs)** to perform advanced analysis in photovoltaics (PV), including **degradation assessment** and **health monitoring**. This project demonstrates how AI can accelerate PV system diagnostics and knowledge extraction from global data sources.

---

## 1. Unified LLM-Based Framework for Heterogeneous PV Image Diagnostics

This project introduces an **open-source multimodal large language model (LLM)–based framework** for automated photovoltaic (PV) image diagnostics across heterogeneous imaging modalities. The framework enables a **single, task-aware inference pipeline** for diverse PV inspection tasks without task-specific model training.

The framework analyzes multiple PV image types, including:

- **Visible images** (bird droppings, surface contamination)
- **Infrared (IR) images** (thermal anomalies, e.g., hotspots)
- **Electroluminescence (EL) images** (microcracks, broken cells)

Key features include **zero-shot and few-shot inference**, **binary and multiclass classification**, and compatibility with state-of-the-art multimodal LLMs (e.g., ChatGPT, Gemini, Claude, CLIP). By eliminating the need for large labeled datasets and retraining, this framework serves as a **rapid pre-screening tool** for scalable PV health monitoring.

**Dataset**: A benchmark dataset of labeled PV images is publicly available at  
https://datahub.duramat.org/dataset/llm-pv-image

**Figure: Multimodal LLM-based PV Image Analysis Flowchart**
<img src="https://github.com/lbj2011/PV-LLM/blob/main/doc_img/image_flowchart.jpg" width="600"/>

---

## 2. Literature Mining: Global PV Degradation Insights

PV-LLM also performs large-scale **literature analysis** using LLMs. The system can:

* Read scientific papers
* Identify and extract degradation rates, technologies, and climates
* Compile global trends in PV degradation

This enables the creation of a unified degradation knowledge base across:

* Regions (e.g., US, EU, Asia)
* Technologies (e.g., mono, poly, thin-film)
* Timescales

**Figure: Global PV Degradation Trends Extracted from Literature**
<img src="https://github.com/lbj2011/PV-LLM/blob/main/doc_img/world_degradation.jpg" width="600"/>

---

## 3. Funding Acknowledgment

This work is supported by the **Durable Module Materials (DuraMAT) Consortium**, a U.S. Department of Energy initiative focused on PV module reliability and innovation.


<img src="https://github.com/lbj2011/PV-LLM/blob/main/doc_img/duramat.jpg" width="200"/>

---

## Contact

For questions or collaboration opportunities, please contact the PV-LLM development team: baojieli@lbl.gov.

---
