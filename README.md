# Recommender Systems Tasks Repository

Welcome to my Recommender Systems repository! 🎬  
This repo contains a collection of practical recommender-system experiments and algorithm implementations, structured as self-contained Jupyter notebooks (.ipynb).  

Each notebook includes inline imports, code commentary, and task explanations.  
Notebooks are best viewed after download — preview is disabled due to their size and output content.  

---

## 📂 Repository Structure  

├── RecSys1_Intro.ipynb  
├── RecSys2_CatBoost_LavkaEvents.ipynb  <br />
├── RecSys3_CanGen.ipynb  <br />
├── RecSys4_NeuralRanking.ipynb  <br />
├── requirements.txt  
├── LICENSE  
└── README.md  

---

## 📑 Task Overview  

| Notebook | Topic | Key Concepts | Notes |
|----------|-------|--------------|-------|
| RecSys1_Intro.ipynb | 🎥 Fundamentals of Recommender Systems | Collaborative Filtering, Jaccard Similarity, Normalized PMI, and Latent Factor Models (SVD) | Implemented base recommender structure and several collaborative filtering variants (user–user, item–item). Explored Jaccard and NPMI similarities, SVD-based latent models. Tasks are inspired by the [Yandex Data School (ШАД) RecSys course](https://github.com/yandexdataschool/recsys_course). The experiments were primarily conducted on IMDb movie data, but the codebase is flexible enough for anime or other domains. |
| RecSys2_CatBoost_LavkaEvents.ipynb | 🛒 Learning to Rank in E-Commerce | Feature Engineering, Train/Validation Splitting without Temporal Leakage, Gradient Boosting (CatBoost), Ranking Metrics (NDCG, Novelty, Serendipity) | Worked with real user interaction logs from the Yandex Lavka app. Built time-aware training sets, engineered behavioral features (CTR, personalized purchase frequency), trained a CatBoost ranking model, and evaluated recommendations using ranking metrics such as NDCG@K, Novelty@K, and Serendipity@K. Demonstrated how relevance and diversity trade-offs influence user experience. |
| RecSys4_NeuralRanking.ipynb | 🧠 Neural Ranking & Deep Feature Encoding | Unified Multisize Embeddings with Hash Collisions, Piecewise Linear Encoding (PLE), Transformer-based Sequence Modeling, DCN-v2 Cross Networks, Pairwise Ranking Loss (Calibrated Pairwise Logistic), CatBoost Baseline Comparison | Extended the classical RecSys pipeline into full neural ranking. Implemented unified embedding tables with controlled multi-feature hashing and analyzed intra- vs inter-feature collision bias. Added Piecewise Linear Encoding (PLE) for numerical features using quantile-based binning and linear mixing. Built user-history encoders (Context, Item, Action), absolute positional encoding, and Transformer architecture for sequence modeling. Implemented Next-Positive Prediction and Feedback Prediction pretraining, then calibrated pairwise logistic finetuning with realistic timestamp lag constraints. Reproduced Yandex School of Data Analysis experiments, validated outputs, and compared neural models to CatBoost ranking baselines. |
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

Launch Jupyter Notebook or Jupyter Lab:

```bash
jupyter notebook
```

Open the notebook (e.g., `RecSys1_Intro.ipynb`).  
Run the cells sequentially — each notebook contains:

- Task formulation  
- Code implementation  
- Result visualization and commentary  

---

## 📊 Implemented Techniques

This repository currently includes implementations of:

- Jaccard-based Collaborative Filtering (user–user & item–item)  
- NPMI (Normalized Pointwise Mutual Information) for penalizing popularity bias  
- Latent Factor Models (Truncated SVD) for dense representation learning  
- Dataset processing with Polars for fast tabular computation  
- Sparse representation and optimization using SciPy CSR matrices  

---

## 🛠 Dependencies

Main libraries used across notebooks:

- numpy, polars, scipy, tensorflow  
- matplotlib, tqdm, PIL, BeautifulSoup  
- requests, kagglehub, concurrent.futures, tensorboard  

See `requirements.txt` for details.

---

## 🌟 Future Work

Planned extensions include:

- Implicit feedback matrix factorization (ALS)  
- Hybrid content–collaborative recommenders  
- Evaluation metrics (MAP@K, NDCG, Recall@K)  
- Advanced embeddings (Word2Vec/GraphSAGE-based models)  
- Visualization of latent spaces via TensorBoard Projector  

---

## 📜 License

This repository is released under the MIT License.  
Feel free to fork, explore, and build upon it!

---

## 👤 Author

Created by **Anastasiia Lapshina**.  
Reference reposityory: https://github.com/yandexdataschool/recsys_course  <br />
Feel free to reach out via GitHub Issues if you’d like to collaborate or discuss recommender-system ideas.
