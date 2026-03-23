# Comparative Topic Modeling of Political Discourse

## Project Overview
This project implements a Natural Language Processing (NLP) pipeline to extract and compare thematic structures from large-scale social media datasets. Using **Latent Dirichlet Allocation (LDA)**, I analyzed the digital discourse of two distinct political figures to identify divergent patterns in populist rhetoric.

## 📊 Technical Metadata
| Category | Details |
| :--- | :--- |
| **Project Type** | Unsupervised Machine Learning / NLP |
| **Data Source** | Twitter/X Archive (Trump & Sanders) |
| **Data Volume** | 5,000+ localized tweets (subset for balanced analysis) |
| **Primary Algorithm** | LDA (Latent Dirichlet Allocation) |
| **Evaluation Metrics** | Coherence Score ($C_v$), Perplexity |
| **Environment** | Linux-based Cloud Environment (Google Colab) |
| **Python Version** | 3.10+ |

## 🛠 Tech Stack & Dependencies
* **Core Logic**: `Python`
* **Data Manipulation**: `Pandas`, `NumPy`
* **NLP Tools**: `NLTK`, `little_mallet_wrapper`
* **Modeling**: `tomotopy` (High-performance C++ implementation for Python)
* **Visualization**: `Seaborn`, `Matplotlib` (Heatmaps, distribution plots)

## ⚙️ Engineering Highlights (IT & Data Focused)
* **Preprocessing Pipeline**: Engineered a robust cleaning script to handle "noisy" social media data, including regex-based filtering for handles (@), URLs (http/https), and non-alphanumeric artifacts.
* **Hardware Efficiency**: Utilized `tomotopy` for its multi-threading capabilities, significantly reducing training time compared to standard `Gensim` implementations.
* **Reproducibility**: Documented random seed states and hyperparameter configurations ($K=5$ to $30$) to ensure consistent model outputs across different runtime sessions.
* **Troubleshooting**: Successfully resolved C++ compiler compatibility issues (common with `tomotopy` on Windows) by configuring a containerized-style workflow in a cloud Linux environment.

## Analysis Workflow
1.  **ETL**: Ingesting JSON/CSV datasets into optimized DataFrames.
2.  **Normalization**: Custom tokenization, stop-word exclusion, and text frequency analysis.
3.  **Model Selection**: Iterative testing of topic counts to maximize the Coherence-vs-Interpretability ratio.
4.  **Deployment-ready Insight**: Exporting topic distributions to structured formats for further downstream analysis.

## Author
**Alex Zhang**
*MA in Digital Communication and Information Studies*
