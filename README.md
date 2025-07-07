# MarketMind: Customer Segmentation using LLM

MarketMind is a customer segmentation pipeline powered by **Large Language Models (LLMs)** and clustering algorithms. It transforms customer data—especially textual attributes—into meaningful segments using semantic understanding, outlier filtering, and unsupervised learning. This empowers marketers and analysts to discover hidden customer groups and derive actionable insights.

---

##  Why Use LLMs for Customer Segmentation?

Traditional clustering methods struggle to deal with unstructured data such as customer reviews, preferences, and behavioral notes. LLMs help overcome this by:

-  **Semantic Embedding**: Transforming raw text into dense, meaningful vector representations.
-  **Context-Aware Grouping**: Capturing hidden intent and behavior patterns from textual data.
-  **Segment Explainability**: Helping generate natural-language summaries for each cluster.

---

## Project Workflow

```mermaid
graph TD
    A[Load Tabular Dataset] --> B[Compile Text using compile_text function]
    B --> C[Load MiniLM SentenceTransformer - all-MiniLM-L6-v2]
    C --> D[Generate Text Embeddings as Dense Vectors]
    D --> E[Outlier Detection using ECOD Model]
    E --> F[Find Optimal K using Elbow Method]
    F --> G[Perform KMeans Clustering]
    G --> H[Visualize Clusters using PCA and t-SNE]
marketmind/
│
├── data/                    # Input datasets
├── images/                  # Visual outputs and architecture diagram
├── models/                 # Saved embeddings or models
├── notebooks/              # Jupyter notebooks (step-by-step demos)
├── src/
│   ├── preprocess.py        # Compile text, clean data
│   ├── embedding.py         # Sentence embedding generation
│   ├── outlier_detection.py # ECOD outlier filtering
│   ├── clustering.py        # Elbow method and KMeans clustering
│   ├── visualize.py         # PCA and t-SNE visualization
│   └── utils.py             # Helper functions
├── main.py                  # Main pipeline execution script
├── requirements.txt         # Project dependencies
└── README.md                # Documentation
