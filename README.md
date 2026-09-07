# Cross-Platform Fake News & Trend Detection using Multimodal Variational Autoencoders (MVAE)

## 📌 Overview

This project presents a **multimodal machine learning framework for fake news detection and trend discovery across different social media platforms**. The system combines **Natural Language Processing (NLP)** and **Computer Vision** to analyze both textual and visual information associated with news articles.

The main objective is to investigate how combining text and image representations can provide a richer understanding of misinformation patterns and improve the analysis of fake news across different domains.

The project uses the **FakeNewsNet dataset**, including articles from **PolitiFact** and **GossipCop**, and employs a custom **Multimodal Variational Autoencoder (MVAE)** to learn compact latent representations from fused textual and visual features.

---

## 🚀 Key Features

* 📊 Uses the **FakeNewsNet dataset** with approximately **23,000 news articles**
* 📝 Performs advanced NLP preprocessing, including text cleaning and lemmatization
* 🔤 Generates **384-dimensional Sentence-BERT embeddings**
* 🖼️ Extracts **1280-dimensional visual features** using a pre-trained **MobileNetV2**
* 🔗 Combines textual and visual features into a **1664-dimensional multimodal representation**
* 🧠 Implements a custom **Variational Autoencoder (VAE)** for multimodal representation learning
* 🎯 Learns compact **32-dimensional latent representations**
* 📉 Uses **PCA and t-SNE** for latent space visualization
* 🔍 Applies **KMeans clustering** for unsupervised trend discovery
* 🤖 Benchmarks multiple machine learning classifiers
* 🌐 Evaluates performance across different platforms and datasets

---

## 🏗️ Methodology

### 1. Text Processing

The textual content of news articles is processed using an NLP pipeline that includes:

* Text cleaning
* Tokenization
* Lemmatization
* Removal of unnecessary information
* Semantic embedding generation using **Sentence-BERT**

Each article is represented as a **384-dimensional textual embedding**.

---

### 2. Image Feature Extraction

Images associated with news articles are processed using a pre-trained **MobileNetV2 Convolutional Neural Network**.

The extracted visual representation contains:

**1280-dimensional image features**

---

### 3. Multimodal Feature Fusion

Textual and visual embeddings are combined to create a unified multimodal representation:

```text
Text Features:   384 dimensions
Image Features: 1280 dimensions
--------------------------------
Total:          1664 dimensions
```

This fused representation captures complementary information from both modalities.

---

### 4. Multimodal Variational Autoencoder (MVAE)

A custom **Variational Autoencoder (VAE)** is trained to learn meaningful and compact representations of the multimodal data.

The architecture includes:

* GELU activation functions
* Batch normalization
* Encoder-decoder architecture
* Variational latent space learning
* 32-dimensional latent representation

The model is trained using a combined reconstruction objective based on:

* Mean Squared Error (MSE)
* Cosine Similarity Loss

The learned latent space is then used for downstream analysis and classification.

---

## 📊 Trend Discovery and Visualization

To explore misinformation patterns in the learned representation space, the project applies:

* **PCA (Principal Component Analysis)**
* **t-SNE (t-Distributed Stochastic Neighbor Embedding)**
* **KMeans Clustering**

These techniques help visualize the latent space and identify potential clusters and trends within multimodal fake news data.

---

## 🤖 Classification Models

The learned latent representations are evaluated using several machine learning models:

* Logistic Regression
* Random Forest
* Support Vector Machine (SVM with RBF Kernel)
* XGBoost

The models are benchmarked to analyze how effectively the learned multimodal latent representations support fake news classification across different platforms.

---

## 🔬 Research Motivation

Fake news often contains information distributed across multiple modalities. Text alone may not capture misleading visual context, while images alone may lack sufficient semantic information.

By combining **textual and visual signals**, this project explores how multimodal representation learning can improve our understanding of misinformation patterns.

The work is also motivated by recent research in multimodal fake news detection, including transformer-based, CNN-based, and adversarial learning approaches designed to improve robustness and cross-domain generalization.

---

## ⚠️ Challenges

Several challenges were observed during the project:

* Class imbalance
* Missing or unavailable article images
* Dataset inconsistencies
* Cross-platform domain differences
* Limited generalization across datasets
* Variations in misinformation patterns between platforms

These challenges highlight important directions for future research in multimodal learning and misinformation detection.

---

## 🔮 Future Work

Possible future extensions include:

* Transformer-based multimodal architectures
* Cross-platform domain adaptation
* GAN-based adversarial training
* Explainable AI (XAI) for fake news detection
* Attention-based multimodal fusion
* Larger and more diverse datasets
* Real-time misinformation and trend detection
* Multimodal foundation models

---

## 🛠️ Technologies Used

* Python
* TensorFlow / Keras
* Scikit-learn
* Sentence-BERT
* MobileNetV2
* XGBoost
* PCA
* t-SNE
* KMeans
* Pandas
* NumPy
* Matplotlib

---

## 📚 Dataset

This project uses the **FakeNewsNet dataset**, containing fake and real news articles collected from:

* **PolitiFact**
* **GossipCop**

FakeNewsNet provides textual, visual, and social context information for research on fake news detection.

---

## 🎯 Key Insight

**Multimodal learning provides a richer representation of misinformation by combining textual and visual information.**

While the results demonstrate the potential of multimodal latent representation learning, challenges such as **class imbalance, dataset limitations, and cross-domain generalization** remain important areas for future research.

---

## 👩‍💻 Author

**Sadaf Zehra**

Research interests include:

* Artificial Intelligence
* Machine Learning
* Deep Learning
* Natural Language Processing
* Multimodal Learning
* Explainable AI
* Trust & Safety
* Fake News Detection
