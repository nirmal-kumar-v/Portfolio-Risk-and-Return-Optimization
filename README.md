# ╔══════════════════════════════════════════════════════════════╗

# O P T I V E S T

# ╚══════════════════════════════════════════════════════════════╝

### Portfolio Risk & Return Optimization Platform

<p align="center">
  <strong>Mathematical intelligence for smarter portfolio construction.</strong>
</p>

<p align="center">
  <a href="https://optivest-psi.vercel.app/">
    <img src="https://img.shields.io/badge/Live_Demo-OptiVest-000000?style=for-the-badge&logo=vercel&logoColor=white" />
  </a>
  <img src="https://img.shields.io/badge/🏆_1st_Prize-CoE_Hackathon-FFD700?style=for-the-badge" />
  <img src="https://img.shields.io/badge/React-19-61DAFB?style=for-the-badge&logo=react&logoColor=white" />
  <img src="https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white" />
</p>

<p align="center">
  <a href="#-overview">Overview</a> •
  <a href="#-the-problem">Problem</a> •
  <a href="#-the-solution">Solution</a> •
  <a href="#-features">Features</a> •
  <a href="#-architecture">Architecture</a> •
  <a href="#-getting-started">Getting Started</a> •
  <a href="#-team">Team</a>
</p>

---

## 🌐 Live Application

### [Launch OptiVest →](https://optivest-psi.vercel.app/)

> Explore the deployed application and interact with the portfolio optimization engine.

---

# 🏆 1st Prize — Centre of Excellence Hackathon

**OptiVest** was developed as a collaborative hackathon project and secured the **1st Prize** at the **Centre of Excellence (CoE) Hackathon conducted by Kongu Engineering College**.

The project was developed by a four-member team with **equal contribution from every member** across ideation, system architecture, frontend engineering, backend engineering, mathematical optimization, testing, documentation, and presentation.

---

# ✦ Overview

**OptiVest** is a full-stack portfolio optimization platform designed to answer a fundamental investment question:

> **How should capital be distributed across a set of assets to balance risk and return?**

Instead of evaluating stocks individually, OptiVest looks at the **portfolio as a mathematical system**.

The platform uses **Modern Portfolio Theory (MPT)**, statistical analysis, Monte Carlo simulation, covariance modeling, and constrained numerical optimization to explore thousands of possible portfolios.

It then identifies mathematically significant portfolio configurations such as:

* **Maximum Sharpe Ratio Portfolio**
* **Minimum Volatility Portfolio**
* **Efficient Frontier**
* **Risk-oriented portfolio allocations**

---

# 🎯 The Problem

Selecting investments based only on individual stock performance can overlook one of the most important aspects of investing:

### **How assets behave together.**

Two stocks can individually have attractive historical returns while producing a highly volatile portfolio when combined.

A portfolio therefore needs to be evaluated across multiple dimensions:

```text
                    ┌──────────────────┐
                    │ Expected Return  │
                    └────────┬─────────┘
                             │
                             ▼
┌──────────────┐      ┌──────────────┐      ┌──────────────┐
│ Asset Risk   │ ───► │  Portfolio   │ ◄─── │ Correlation  │
└──────────────┘      │    Risk      │      └──────────────┘
                      └──────┬───────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │ Asset Allocation │
                    └──────────────────┘
```

Manually exploring thousands of possible allocations is inefficient.

**OptiVest automates this exploration.**

---

# 💡 The Solution

OptiVest converts historical market data into a quantitative portfolio analysis pipeline.

```text
┌─────────────────────────────────────────────────────────┐
│                    USER INPUT                           │
│                                                         │
│              Selected Stocks / Assets                  │
└────────────────────────┬────────────────────────────────┘
                         │
                         ▼
┌─────────────────────────────────────────────────────────┐
│                  MARKET DATA                            │
│                                                         │
│              Historical Price Series                    │
└────────────────────────┬────────────────────────────────┘
                         │
                         ▼
┌─────────────────────────────────────────────────────────┐
│                STATISTICAL ENGINE                       │
│                                                         │
│       Returns • Volatility • Covariance Matrix         │
└────────────────────────┬────────────────────────────────┘
                         │
                         ▼
┌─────────────────────────────────────────────────────────┐
│             MONTE CARLO SIMULATION                      │
│                                                         │
│              10,000 Portfolio Samples                   │
└────────────────────────┬────────────────────────────────┘
                         │
                         ▼
┌─────────────────────────────────────────────────────────┐
│                EFFICIENT FRONTIER                       │
│                                                         │
│          Risk ↔ Return Portfolio Landscape             │
└────────────────────────┬────────────────────────────────┘
                         │
              ┌──────────┴──────────┐
              ▼                     ▼
      Maximum Sharpe         Minimum Volatility
              │                     │
              └──────────┬──────────┘
                         ▼
                Risk Preference
                         │
                         ▼
                Portfolio Allocation
```

---

# 🚀 Features

## 01 — Portfolio Optimization

OptiVest uses **Modern Portfolio Theory** to analyze the relationship between expected return and portfolio risk.

The engine calculates:

* Expected return
* Portfolio volatility
* Sharpe ratio
* Asset weights
* Covariance
* Portfolio-level risk

---

## 02 — 10,000 Portfolio Simulations

Rather than evaluating only a few manually selected allocations, OptiVest explores **10,000 simulated portfolios**.

Each portfolio receives:

```text
┌─────────────────────────────┐
│ Expected Return             │
│ Volatility                  │
│ Sharpe Ratio                │
│ Asset Allocation            │
└─────────────────────────────┘
```

These portfolios create the visual landscape from which the efficient frontier can be analyzed.

---

## 03 — Efficient Frontier

The efficient frontier represents portfolios that provide the best available expected return for a given level of modeled risk.

Conceptually:

```text
Expected
Return
  ▲
  │
  │                         ●
  │                    ● ●
  │                 ●
  │              ●
  │           ●
  │        ●
  │     ●
  │  ●
  └──────────────────────────────────► Risk
```

This gives users a portfolio-level view rather than evaluating assets in isolation.

---

## 04 — Maximum Sharpe Ratio

OptiVest uses constrained numerical optimization to find the portfolio with the highest modeled Sharpe ratio.

```text
                    MAX SHARPE
                        ●
                       / \
                      /   \
                     /     \
                    /       \
──────────────────────────────────
```

The optimization engine uses:

```python
scipy.optimize.minimize()
```

with the **SLSQP** algorithm.

---

## 05 — Minimum Volatility

The optimization engine also searches for the allocation that minimizes portfolio volatility.

```text
                    Efficient Frontier
                         ●
                      ●
                   ●
                ●
             ●
          ●
       ●
    ●
   │
   │ Minimum Volatility
   ●
──────────────────────────────────► Risk
```

This provides a second mathematically optimized reference portfolio.

---

## 06 — Risk-Based Portfolio Selection

OptiVest allows the optimization results to be interpreted through different risk preferences.

```text
LOW RISK
   │
   │    Capital preservation / lower modeled volatility
   ▼
MEDIUM RISK
   │
   │    Balanced risk-return profile
   ▼
HIGH RISK
   │
   │    Greater modeled return / volatility exposure
   ▼
```

The platform maps the selected risk preference to an appropriate point in the modeled portfolio space.

---

## 07 — Interactive Visualization

The frontend turns the mathematical results into an interactive dashboard.

Visual analytics include:

* Efficient frontier
* Risk-return distribution
* Portfolio allocation
* Asset weights
* Return metrics
* Volatility metrics
* Sharpe ratio
* Optimization results

---

## 08 — Automated PDF Reports

Portfolio analysis can be exported as a PDF report.

This allows the generated analysis to be:

* Saved
* Shared
* Presented
* Archived

without manually reproducing the results.

---

# 🧠 Mathematical Engine

OptiVest is built around **Modern Portfolio Theory**.

For portfolio weights:

```text
w₁, w₂, ..., wₙ
```

the expected portfolio return is:

```text
E(Rₚ) = Σ wᵢE(Rᵢ)
```

Portfolio variance:

```text
σₚ² = wᵀΣw
```

where:

```text
w = portfolio weight vector

Σ = covariance matrix
```

Portfolio volatility:

```text
σₚ = √(wᵀΣw)
```

Sharpe ratio:

```text
Sharpe Ratio = (Rₚ − Rf) / σₚ
```

The optimization engine searches for portfolio weights subject to the defined constraints.

---

# 🔬 Optimization Pipeline

```text
                  Historical Prices
                         │
                         ▼
                  Daily Returns
                         │
                         ▼
                 Annualized Returns
                         │
                         ▼
                Covariance Matrix
                         │
                         ▼
             ┌───────────────────────┐
             │ Monte Carlo Engine    │
             │                       │
             │ 10,000 Portfolios     │
             └───────────┬───────────┘
                         │
                         ▼
                  Risk / Return Cloud
                         │
                         ▼
                 Efficient Frontier
                         │
              ┌──────────┴──────────┐
              │                     │
              ▼                     ▼
        Max Sharpe             Min Volatility
              │                     │
              └──────────┬──────────┘
                         ▼
                 Risk Preference
                         │
                         ▼
                 Final Allocation
```

---

# 🏗 System Architecture

```text
                         OPTIVEST
                            │
            ┌───────────────┴────────────────┐
            │                                │
            ▼                                ▼
     ┌──────────────┐                 ┌──────────────┐
     │   FRONTEND   │                 │   BACKEND    │
     │              │                 │              │
     │ React 19     │ ◄──── REST ───► │ FastAPI      │
     │ Vite         │                 │ Python       │
     │ Tailwind     │                 │              │
     │ Recharts     │                 │ MPT Engine   │
     └──────────────┘                 └──────┬───────┘
                                             │
                           ┌─────────────────┼─────────────────┐
                           │                 │                 │
                           ▼                 ▼                 ▼
                     Yahoo Finance      NumPy/Pandas       SciPy
                       yfinance          Data Engine     Optimizer
                           │
                           ▼
                    Historical Prices
```

---

# 🧩 Technology Stack

## Frontend

| Technology          | Role                          |
| ------------------- | ----------------------------- |
| **React 19**        | Application UI                |
| **Vite**            | Development and build tooling |
| **Tailwind CSS**    | UI styling                    |
| **React Router**    | Application routing           |
| **Axios**           | API communication             |
| **Recharts**        | Data visualization            |
| **Framer Motion**   | Interface animation           |
| **Lucide Icons**    | UI iconography                |
| **React Hook Form** | Form management               |

## Backend

| Technology       | Role                   |
| ---------------- | ---------------------- |
| **FastAPI**      | REST API               |
| **Python**       | Core backend           |
| **yfinance**     | Market data            |
| **Pandas**       | Data manipulation      |
| **NumPy**        | Numerical computation  |
| **SciPy**        | Portfolio optimization |
| **Scikit-learn** | Statistical utilities  |
| **Uvicorn**      | ASGI server            |
| **ReportLab**    | PDF generation         |

---

# 🛡 Data Reliability & Demo Resilience

A major design consideration was the reliability of external market-data APIs.

A hackathon demonstration should not become unusable simply because an external service is temporarily unavailable.

OptiVest therefore implements a fallback data layer.

```text
                 Request Market Data
                         │
                         ▼
                    yfinance
                         │
                ┌────────┴────────┐
                │                 │
             SUCCESS            FAILURE
                │                 │
                ▼                 ▼
          Live Market       Seeded Synthetic
             Data                Data
                │                 │
                └────────┬────────┘
                         ▼
                  Optimization
                         │
                         ▼
                    Dashboard
```

When synthetic data is used, the backend explicitly returns:

```json
{
  "is_simulated_data": true
}
```

The frontend surfaces this state to the user.

This prevents simulated market data from silently appearing to be live market data.

---

# 📂 Project Structure

```text
optivest/
│
├── backend/
│   │
│   ├── main.py
│   ├── requirements.txt
│   ├── ...
│   │
│   └── Portfolio Optimization Engine
│
├── frontend/
│   │
│   ├── src/
│   ├── public/
│   ├── package.json
│   ├── vite.config.js
│   └── ...
│
├── .gitignore
└── README.md
```

---

# 🔌 API

| Method | Endpoint      | Description                |
| ------ | ------------- | -------------------------- |
| `GET`  | `/`           | Backend health check       |
| `GET`  | `/stocks`     | Retrieve available stocks  |
| `POST` | `/optimize`   | Run portfolio optimization |
| `POST` | `/report/pdf` | Generate PDF analysis      |

FastAPI automatically provides interactive API documentation:

```text
http://127.0.0.1:8000/docs
```

---

# ⚙️ Getting Started

## Requirements

Make sure you have:

```text
Python 3.x
Node.js
npm
Git
```

---

## 1. Clone the Repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd optivest
```

---

## 2. Start the Backend

```bash
cd backend
```

Create a virtual environment:

```bash
python -m venv venv
```

### Windows

```bash
venv\Scripts\activate
```

### Linux / macOS

```bash
source venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Start FastAPI:

```bash
uvicorn main:app --reload --port 8000
```

Backend:

```text
http://127.0.0.1:8000
```

API documentation:

```text
http://127.0.0.1:8000/docs
```

---

## 3. Start the Frontend

Open another terminal:

```bash
cd frontend
npm install
npm run dev
```

Frontend:

```text
http://127.0.0.1:5173
```

---

# 🚀 Production Build

```bash
cd frontend
npm run build
```

The optimized production application will be generated inside:

```text
frontend/dist
```

Preview it locally:

```bash
npm run preview
```

---

# ☁️ Deployment

## Frontend

The frontend can be deployed to platforms such as:

* Vercel
* Netlify
* Cloudflare Pages

Build:

```bash
npm run build
```

Deploy:

```text
frontend/dist
```

For separate frontend/backend deployments, configure:

```text
VITE_API_URL=<YOUR_DEPLOYED_BACKEND_URL>
```

---

## Backend

The FastAPI backend can be hosted on platforms such as:

* Render
* Railway
* Fly.io
* AWS EC2

Production command:

```bash
uvicorn main:app --host 0.0.0.0 --port $PORT
```

Configure CORS to allow requests from the deployed frontend.

---

# 🖥️ Live Demo

<p align="center">

### Experience OptiVest

<a href="https://optivest-psi.vercel.app/">

<img src="https://img.shields.io/badge/OPEN_LIVE_DEMO-OPTIVEST-000000?style=for-the-badge&logo=vercel&logoColor=white" />

</a>

</p>

**Live Application:**
https://optivest-psi.vercel.app/

---

# 🏆 Hackathon Achievement

## Centre of Excellence Hackathon

### 🥇 1st Prize

OptiVest was developed and presented at the **Centre of Excellence Hackathon conducted by Kongu Engineering College**.

The project brought together:

```text
Quantitative Finance
        +
Mathematical Optimization
        +
Full-Stack Engineering
        +
Data Visualization
        +
Product Design
```

The entire system was designed, implemented, tested, and presented collaboratively by the team.

---

# 👥 Team

## Team OptiVest

| #      | Team Member        |
| ------ | ------------------ |
| **01** | **Niranjan G**     |
| **02** | **Nirmal Kumar V** |
| **03** | **Nithish**        |
| **04** | **Pranesh Deepan** |

### Equal Contribution

All four members contributed equally to the project.

Our collective contributions covered:

* Product ideation
* System architecture
* Frontend engineering
* Backend engineering
* Quantitative modeling
* Portfolio optimization
* Data processing
* Visualization
* UI/UX
* Testing
* Documentation
* Hackathon presentation

---

# 🔮 Future Roadmap

OptiVest can be extended into a broader portfolio intelligence platform.

### Portfolio Intelligence

* Live portfolio tracking
* Portfolio history
* Automated rebalancing
* Performance attribution
* Portfolio backtesting

### Advanced Risk Analytics

* Value at Risk — VaR
* Conditional VaR
* Maximum Drawdown
* Beta analysis
* Sortino Ratio
* Downside deviation

### Advanced Optimization

* Black-Litterman model
* Risk parity
* Sector constraints
* Transaction-cost optimization
* Factor-based optimization
* Custom investor constraints

### Platform Features

* User authentication
* Persistent portfolios
* Cloud database
* Portfolio sharing
* Scheduled reports
* Real-time market monitoring
* Broker/API integration

---

# ⚠️ Disclaimer

OptiVest is a **hackathon demonstration and educational project**.

The portfolio calculations are based on historical data, mathematical assumptions, and simulated scenarios where applicable.

Historical performance does not guarantee future results.

Nothing presented by OptiVest should be considered financial, investment, or trading advice.

Users should conduct independent research and consult a qualified financial professional before making investment decisions.

---

# ⭐ Support the Project

If you find OptiVest interesting:

**⭐ Star the repository**

**🍴 Fork the project**

**🧑‍💻 Explore the implementation**

**🌐 Try the live demo**

---

<p align="center">

## OPTIVEST

### Analyze. Optimize. Understand Risk.

**Built with mathematics, engineering, and teamwork.**

<br>

🏆 **1st Prize — Centre of Excellence Hackathon**

</p>
