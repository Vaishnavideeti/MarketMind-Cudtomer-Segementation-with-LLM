#  MarketMind: Customer Segmentation using LLM

MarketMind is a customer segmentation pipeline powered by **Large Language Models (LLMs)** and clustering algorithms. It transforms customer data—especially textual attributes—into meaningful segments using semantic understanding, outlier filtering, and unsupervised learning. This empowers marketers and analysts to discover hidden customer groups and derive actionable insights.

---

##  Why Use LLMs for Customer Segmentation?

Traditional clustering struggles with unstructured data like reviews, feedback, or descriptions. LLMs overcome this by:

-  **Semantic Embedding**: Transforming raw text into dense, meaningful vector representations.
-  **Context-Aware Grouping**: Capturing hidden intent and behavior patterns from text data.
-  **Segment Explainability**: Helping auto-label segments using natural language generation.

---

## 🔁 Project Workflow

```mermaid
graph TD;
    A[Load Tabular Dataset] --> B[Compile Text from Rows using `compile_text`];
    B --> C[Load MiniLM SentenceTransformer ('all-MiniLM-L6-v2')];
    C --> D[Generate Embeddings (Text → Dense Vectors)];
    D --> E[Outlier Detection using ECOD Model];
    E --> F[Find Optimal K using Elbow Method];
    F --> G[Perform KMeans Clustering];
    G --> H[Visualize Clusters using PCA and t-SNE];
