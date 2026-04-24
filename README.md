# Recommender Systems Tasks Repository

Welcome to my Recommender Systems repository! 🎬  
This repo contains a collection of practical recommender-system experiments and algorithm implementations, structured as self-contained Jupyter notebooks (`.ipynb`).

Each notebook includes inline imports, code commentary, and task explanations.  
Notebooks are best viewed after download — preview may be limited due to notebook size and saved outputs.

The **DeepRecSys** notebooks in this repository were inspired by and completed as part of the **DeepRecSys course (HSE)** based on the following course materials:  
https://github.com/KhrylchenkoKirill/DeepRecSys/tree/main

---

## 📂 Repository Structure

├── DeepRecSys1.ipynb  
├── DeepRecSys2.ipynb  
├── RecSys1_Intro.ipynb  
├── RecSys2_CatBoost_LavkaEvents.ipynb  
├── RecSys3_CanGen.ipynb  
├── RecSys4_NeuralRanking.ipynb  
├── requirements.txt  
├── LICENSE  
└── README.md  

---

## 📑 Task Overview

| Notebook | Topic | Key Concepts | Notes |
|----------|-------|--------------|-------|
| DeepRecSys1.ipynb | 🎧 Retrieval for Sequential Recommendation | Data preparation, ranking metrics, TopPop, collaborative filtering, item-to-item retrieval, Item2Vec, cosine similarity, TF-IDF weighting, ALS, leaderboard-based comparison | Covers the full basic retrieval pipeline: data preparation → metric implementation → several retrieval approaches → final leaderboard. Implemented and compared TopPop, user-artist heuristics, item-to-item retrieval from dataset embeddings, Item2Vec, collaborative filtering with cosine similarity, TF-IDF reweighting, and ALS-based recommenders. Completed as part of the **DeepRecSys (HSE)** course. |
| DeepRecSys2.ipynb | 🧠 Two-Tower Retrieval & Sampled Objectives | Sequential datasets, flatten batching, user-history encoding, two-tower retrieval, full softmax, sampled softmax, BCE, BPR, in-batch negatives, logQ correction, fixed logQ correction | Implements a neural retrieval pipeline based on a two-tower model for next-item prediction. Explores several training objectives and sampling strategies, including full softmax, sampled softmax, BCE, BPR, in-batch negatives, and popularity-bias correction via logQ / fixed logQ. Also includes bonus tasks on improving user-history aggregation. Completed as part of the **DeepRecSys (HSE)** course. |
| RecSys1_Intro.ipynb | 🎥 Fundamentals of Recommender Systems | Collaborative Filtering, Jaccard Similarity, Normalized PMI, latent factor models (SVD) | Implemented a base recommender structure and several collaborative filtering variants (user-user, item-item). Explored Jaccard and NPMI similarities, as well as SVD-based latent models. Tasks are inspired by the [Yandex Data School (ШАД) RecSys course](https://github.com/yandexdataschool/recsys_course). Experiments were primarily conducted on IMDb movie data, but the codebase is flexible enough for other domains. |
| RecSys2_CatBoost_LavkaEvents.ipynb | 🛒 Learning to Rank in E-Commerce | Feature engineering, train/validation splitting without temporal leakage, gradient boosting (CatBoost), ranking metrics (NDCG, Novelty, Serendipity) | Worked with real user interaction logs from the Yandex Lavka app. Built time-aware training sets, engineered behavioral features (CTR, personalized purchase frequency), trained a CatBoost ranking model, and evaluated recommendations with ranking metrics such as NDCG@K, Novelty@K, and Serendipity@K. |
| RecSys3_CanGen.ipynb | ⚡ Candidate Generation for Recommendation Systems | Retrieval-stage design, scalable candidate generation, evaluation of candidate generators | Focuses on the candidate generation stage of a recommender pipeline: how to retrieve a manageable set of plausible items efficiently before ranking. Includes practical experiments and comparisons of retrieval strategies under realistic constraints. |
| RecSys4_NeuralRanking.ipynb | 🧩 Neural Ranking & Deep Feature Encoding | Unified multisize embeddings with hash collisions, piecewise linear encoding (PLE), Transformer-based sequence modeling, DCN-v2 cross networks, pairwise ranking loss, CatBoost comparison | Extends the classical RecSys pipeline into neural ranking. Implements unified embedding tables with controlled multi-feature hashing, analyzes intra- vs inter-feature collision bias, adds PLE for numerical features, builds user-history encoders with positional encoding and Transformer layers, and compares neural rankers to CatBoost baselines. |

---

## ⚙️ Setup & Installation

To run the notebooks locally, you’ll need Python 3.9+ and the dependencies listed in `requirements.txt`.

```bash
git clone https://github.com/yourusername/recsys-tasks.git
cd recsys-tasks
pip install -r requirements.txt
```

Alternatively, you can open notebooks directly in Google Colab — all imports are provided inline.

---

## 🧑‍💻 Usage

Launch Jupyter Notebook or JupyterLab:

```bash
jupyter notebook
```

Open the notebook you want to run (for example, `DeepRecSys1.ipynb` or `DeepRecSys2.ipynb`) and execute cells sequentially.  
Each notebook includes:

- task formulation
- code implementation
- metric computation
- experimental comparison and commentary

---

## 📊 Implemented Techniques

This repository currently includes implementations of:

- TopPop recommendation
- User-artist heuristic recommenders
- Item-to-item retrieval from dataset embeddings
- Item2Vec / Word2Vec-based item embeddings
- Collaborative filtering with cosine similarity
- TF-IDF weighting for collaborative filtering
- Alternating Least Squares (ALS), both raw and TF-IDF-weighted
- Jaccard-based collaborative filtering (user-user & item-item)
- NPMI (Normalized Pointwise Mutual Information) for popularity-aware similarity
- Latent factor models (Truncated SVD)
- Two-tower neural retrieval
- Full softmax, sampled softmax, BCE, and BPR training objectives
- In-batch negatives
- logQ and fixed logQ correction
- Dataset processing with Polars
- Sparse optimization using SciPy CSR matrices

---

## 🛠 Dependencies

Main libraries used across notebooks include:

- numpy
- polars
- scipy
- pandas
- torch / torchvision
- tensorflow
- gensim
- scikit-learn
- catboost
- matplotlib
- tqdm
- PIL
- BeautifulSoup
- requests
- kagglehub
- tensorboard

See `requirements.txt` for the exact environment.

---

## 🌟 Future Work

Potential future extensions include:

- hybrid content-collaborative retrieval pipelines
- session-based recommenders with stronger sequential encoders
- advanced retrieval/ranking distillation
- multi-task ranking objectives
- approximate nearest-neighbor retrieval for dense embeddings
- richer cold-start handling for new users and new items
- graph-based recommenders (for example, GraphSAGE / LightGCN-style approaches)
- visualization of learned latent spaces via TensorBoard Projector

---

## 📜 License

This repository is released under the MIT License.  
Feel free to fork, explore, and build upon it.

---

## 👤 Author

Created by **Anastasiia Lapshina**.

Reference repositories and course materials:
- DeepRecSys course (HSE): https://github.com/KhrylchenkoKirill/DeepRecSys/tree/main
- Yandex Data School RecSys course: https://github.com/yandexdataschool/recsys_course

Feel free to reach out via GitHub Issues if you’d like to collaborate or discuss recommender-system ideas.
