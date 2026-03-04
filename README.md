# 🎵 Bop-App  
**AI-Powered Swipe-Based Music Recommendation System**

Bop-App is a machine learning–driven music recommendation application where users swipe right (like) or left (dislike) on songs. The system continuously learns user preferences and generates personalized music recommendations in real time.

This project demonstrates applied machine learning, recommendation systems, personalization, and Retrieval-Augmented Generation (RAG) concepts in a production-style architecture.

---

## 🚀 Features

- 🎯 Swipe-based feedback collection (implicit preference learning)
- 🤖 Hybrid recommendation system (collaborative + content-based)
- 🔄 Real-time user preference embedding updates
- 🧊 Cold-start handling for new users and songs
- 📊 Model evaluation (Precision@K, Recall@K, ROC-AUC)
- 🧠 Personalized RAG for contextual playlist generation
- ⚡ Fast similarity search using vector embeddings

---

## 🏗️ System Architecture

### 1️⃣ Data Collection

User interactions:
- Right swipe → Positive feedback
- Left swipe → Negative feedback

Interactions are stored in a user-item matrix and logged for model training.

---

### 2️⃣ Recommendation Engine

#### 🔹 Collaborative Filtering
- Matrix factorization (SVD / ALS)
- Learns latent embeddings for users and songs
- Captures hidden preference patterns

#### 🔹 Content-Based Filtering
- Uses song metadata:
  - Genre
  - Tempo
  - Mood
  - Artist
- Extracts audio features (MFCCs, spectral features)
- Computes cosine similarity between song vectors

#### 🔹 Hybrid Ranking
Final recommendations combine:
- User latent embedding score
- Content similarity score
- Popularity prior (for cold-start)

---

### 3️⃣ Personalization Engine

Each user has a dynamic preference vector that updates after every swipe:

- Like → Move embedding toward song vector  
- Dislike → Move embedding away from song vector  

This enables continuous real-time adaptation.

---

### 4️⃣ Personalized RAG (Retrieval-Augmented Generation)

To enhance explainability and engagement:

**Step 1: Retrieve**
- User listening history
- Song metadata
- Artist information

**Step 2: Generate**
- Personalized playlist descriptions
- Mood-based summaries
- “Why you’ll like this” explanations

This combines recommendation systems with LLM-based generation.

---

## 📈 Machine Learning Components

- Matrix Factorization (SVD / ALS)
- Like-prediction classification model
- Cosine similarity ranking
- Approximate Nearest Neighbor (ANN) search
- Clustering (K-Means) for taste profiling
- Reinforcement-style reward optimization
- A/B testing simulations

---

## 📊 Evaluation Metrics

- Precision@K
- Recall@K
- ROC-AUC
- Engagement rate
- Swipe-to-like conversion ratio

---

## 🧊 Cold Start Strategy

### New Users
- Popularity-based recommendations
- Genre onboarding selection
- Content similarity bootstrapping

### New Songs
- Audio feature embedding similarity
- Metadata-based similarity scoring

---

## 🛠️ Tech Stack

- Python  
- NumPy  
- Pandas  
- Scikit-learn / PyTorch  
- FastAPI  
- FAISS (vector search)  
- REST APIs  

---

## 📂 Project Structure
