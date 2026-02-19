# Time-Series Forecasting

> End-to-end pipeline for GitHub repository metrics analysis and forecasting. Ingests two years of issue, pull-request, commit, branch, contributor, and release data via the GitHub API. Compares three forecasting engines—LSTM, Prophet, and Holt–Winters—with MAE/RMSE on a 30-day hold-out. Includes interactive visualizations, Flask microservice, React dashboard, and CI/CD automation.

---

## Features

- **Data pipeline** — Ingests two years of GitHub issue, pull-request, commit, branch, contributor, and release data via the GitHub API
- **Forecasting engines** — LSTM (TensorFlow/Keras), Prophet, Holt–Winters (StatsModels), evaluated with MAE and RMSE on 30-day hold-out
- **Visualizations** — Daily, weekly, and monthly issue trends; stacked and grouped bar charts; 7- to 30-day forecasts by weekday and month
- **Deployment** — Flask microservice for data processing and model serving; React frontend for dashboarding; Docker containers on Google Cloud Run
- **Automation** — CI/CD to rebuild, retrain, and redeploy forecasts when new GitHub data arrive

---

## Repositories Tracked

| Repository |
|------------|
| [meta-llama/llama3](https://github.com/meta-llama/llama3) |
| [ollama/ollama](https://github.com/ollama/ollama) |
| [langchain-ai/langchain](https://github.com/langchain-ai/langchain) |
| [langchain-ai/langgraph](https://github.com/langchain-ai/langgraph) |
| [microsoft/autogen](https://github.com/microsoft/autogen) |
| [openai/openai-cookbook](https://github.com/openai/openai-cookbook) |
| [elastic/elasticsearch](https://github.com/elastic/elasticsearch) |
| [milvus-io/pymilvus](https://github.com/milvus-io/pymilvus) |

---

## Quick Start

### Prerequisites

- Python 3.8+
- [GitHub Personal Access Token](https://github.com/settings/tokens)

### Setup

```bash
git clone https://github.com/YOUR_USERNAME/Time-Series-Forecasting.git
cd Time-Series-Forecasting

python -m venv .venv
.venv\Scripts\activate          # Windows
# source .venv/bin/activate     # macOS/Linux

pip install -r requirements.txt
```

### Environment

Create a `.env` file:

```env
GITHUB_TOKEN=ghp_your_token_here
```

### Run

```bash
jupyter notebook GitHub_Repos_Issues_Forecasting_clean.ipynb
# or
jupyter lab
```

Run all cells to fetch data and generate forecasts.

---

## Project Structure

```
Time-Series-Forecasting/
├── GitHub_Repos_Issues_Forecasting_clean.ipynb   # Main notebook
├── requirements.txt
├── .env                                         # GITHUB_TOKEN (create locally)
└── README.md
```

### Notebook Sections

| Section | Content |
|---------|---------|
| **1. Data Ingestion** | GitHub API fetch (issues, PRs, commits, etc.) |
| **2–7. EDA** | Issue trends, monthly/weekly charts, stars, forks |
| **8. LSTM** | TensorFlow/Keras forecasting (30-day horizon) |
| **9. Prophet** | Facebook Prophet forecasting |
| **10. Holt–Winters** | StatsModels exponential smoothing |

---

## Tech Stack

| Category | Technologies |
|----------|--------------|
| **Language** | Python |
| **Data** | NumPy, Pandas |
| **ML/Forecasting** | TensorFlow/Keras, Prophet, StatsModels |
| **Visualization** | Matplotlib |
| **API** | GitHub API (PyGithub, github3.py) |
| **Deployment** | Flask, React.js, Docker, GCP Cloud Run |

---

