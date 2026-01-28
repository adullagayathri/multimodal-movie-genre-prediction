#  Multimodal Movie Genre Prediction

A deep learning project that predicts **movie genres** by combining **text (plot overview)** and **vision (poster images)** using multimodal fusion techniques in PyTorch. This model captures semantic and visual cues to improve multi‑label genre classification accuracy over unimodal approaches, and results are exposed through a web interface.

---

##  Problem Statement

Movie genre prediction is a **multi-label classification problem**: each movie can belong to multiple genres simultaneously (e.g., Action + Comedy). Leveraging both textual and visual information leads to richer representations and better generalization compared to single-modality models.

This repository implements a **fusion model** using:
- Text features from movie overviews  
- Image features from movie posters  
- Deep learning architectures for both modalities  

The goal is to improve genre prediction performance by integrating complementary signals from text and visuals.

---

##  Key Features

-  **Multimodal fusion architecture** combining DistilBERT embeddings and a ResNet-based vision encoder  
-  Integrated preprocessing for text and poster image inputs  
-  End-to-end model training and evaluation pipeline  
-  Support for multi-label classification with co-occurrence and imbalance handling  
-  Interactive demo (live site hosted via GitHub Pages)

---

##  Repository Structure
- ├── data/
- │ └── tmdb_cleaned_final.csv <- Dataset used for training and evaluation
- ├── images/ <- Example plots/posters for documentation
- ├── fusion_code.ipynb <- Model training & fusion implementation
- ├── fusion_data_cleaning.ipynb <- Data preprocessing notebooks
- ├── data_text_model.ipynb <- Text-only model experiments
- ├── fusion_inference_script.ipynb <- Inference workflow and prediction examples
- ├── index.html <- Hosted demo web UI
- ├── styles.css <- UI styling for demo
- └── README.md

---

##  Methodology

### 1. Text Modality
- Tokenized raw movie overviews
- Extracted contextual embeddings using pretrained language models (DistilBERT)
- Fine-tuned embeddings for multi-label genre classification

### 2. Vision Modality
- Processed poster images
- Extracted visual features with pretrained CNN architectures (ResNet-18)
- Fine-tuned visual embeddings for genre prediction

### 3. Multimodal Fusion
- Concatenated text and image embeddings
- Trained a joint classifier on fused features
- Applied strategies for class imbalance and co-occurrence dependencies

> This fusion approach captures both **semantic meaning from text** and **visual genre cues**, leading to better predictions.

---

##  Results & Evaluation

Model performance and comparisons are documented in the evaluation notebooks (`fusion_code.ipynb`). Metrics include:
- **Macro & Micro F1-score**
- **Precision & Recall per genre**
- **Confusion matrix analyses**

Graphs and tables demonstrate improvements over unimodal baselines.

---

##  Live Demo

The project includes a hosted interactive interface:

 [Live Demo](https://adullagayathri.github.io/multimodal-movie-genre-prediction/)

Users can upload a movie poster and enter an overview to receive genre predictions.

---

##  Tech Stack

- **Deep Learning:** PyTorch, Transformers (DistilBERT)  
- **Computer Vision:** ResNet-based encoders  
- **Data Processing:** Pandas, NumPy  
- **Notebook Environment:** Jupyter  
- **Web Demo:** HTML, CSS (GitHub Pages)

---

##  Getting Started

1. Clone the repository  
   ```bash
   git clone https://github.com/adullagayathri/multimodal-movie-genre-prediction.git
   cd multimodal-movie-genre-prediction


