# Time-Series Forecasting

End-to-end pipeline for GitHub repository metrics analysis and forecasting. Ingests two years of issue, pull-request, commit, branch, contributor, and release data via the GitHub API. Compares LSTM, Prophet, and Holt-Winters with MAE and RMSE on a 30-day hold-out. Includes interactive visualizations, Flask microservice, React dashboard, and CI/CD automation.

## Features

- **Data pipeline:** Ingest two years of GitHub data (issues, PRs, commits, branches, contributors, releases) via the API
- **Forecasting:** LSTM (TensorFlow/Keras), Prophet, Holt-Winters (StatsModels) with MAE/RMSE on 30-day hold-out
- **Visualizations:** Daily, weekly, monthly trends; stacked and grouped bar charts; 7-30 day forecasts by weekday and month
- **Deployment:** Flask microservice, React frontend, Docker on Google Cloud Run
- **CI/CD:** Rebuild, retrain, redeploy when new data arrive

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

## Quick Start

**Prerequisites:** Python 3.8+, [GitHub Personal Access Token](https://github.com/settings/tokens)

```bash
git clone https://github.com/YOUR_USERNAME/Time-Series-Forecasting.git
cd Time-Series-Forecasting

python -m venv .venv
.venv\Scripts\activate   # Windows
# source .venv/bin/activate   # macOS/Linux

pip install -r requirements.txt
```

Create a `.env` file with `GITHUB_TOKEN=ghp_your_token_here`. Do not commit it.

```bash
jupyter notebook GitHub_Repos_Issues_Forecasting_clean.ipynb
```

Run all cells to fetch data and generate forecasts.

## Project Structure

```
Time-Series-Forecasting/
├── GitHub_Repos_Issues_Forecasting_clean.ipynb
├── requirements.txt
└── README.md
```

## Notebook Sections

| Section | Content |
|---------|---------|
| 1. Data Ingestion | GitHub API fetch |
| 2-7. EDA | Issue trends, charts, stars, forks |
| 8. LSTM | TensorFlow/Keras forecasting |
| 9. Prophet | Facebook Prophet |
| 10. Holt-Winters | StatsModels exponential smoothing |

## Tech Stack

Python, NumPy, Pandas, TensorFlow/Keras, Prophet, StatsModels, Matplotlib, Flask, React.js, Docker, Google Cloud Platform
