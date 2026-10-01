<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Space+Grotesk&weight=600&size=34&duration=2800&pause=900&color=7C3AED&center=true&vCenter=true&width=800&lines=OPTIVEST;Risk+%26+Return+Intelligence;Mathematical+Portfolio+Optimization;Built+to+Understand+Risk." alt="OptiVest" />

<br>

### **PORTFOLIO RISK & RETURN INTELLIGENCE**

<br>

<a href="https://optivest-psi.vercel.app/">
<img src="https://img.shields.io/badge/%E2%86%92%20EXPLORE%20OPTIVEST-111111?style=for-the-badge&labelColor=111111&color=7C3AED" />
</a>

<br><br>

<img src="https://img.shields.io/badge/%F0%9F%A5%87%201ST%20PRIZE-CENTRE%20OF%20EXCELLENCE%20HACKATHON-111111?style=for-the-badge&labelColor=111111&color=F5B942" />

</div>

<br>

---

<div align="center">

## **OPTIMIZE THE PORTFOLIO.**

## **UNDERSTAND THE RISK.**

<br>

**OptiVest** is a full-stack quantitative portfolio intelligence platform that transforms historical market data into mathematically optimized portfolio allocations using **Modern Portfolio Theory**.

<br>

`10,000+ SIMULATED PORTFOLIOS`    `EFFICIENT FRONTIER`    `MAX SHARPE`    `MIN VOLATILITY`

</div>

<br>

---

## ✦ The Idea

Most portfolio decisions start with a simple question:

> **“Which stock should I buy?”**

OptiVest approaches the problem differently.

It asks:

> **“How should multiple assets work together inside a portfolio?”**

Instead of looking at assets independently, OptiVest analyzes **return, volatility, covariance and portfolio-level risk** to explore thousands of possible allocations.

The result is an interactive risk-return intelligence layer built around **Modern Portfolio Theory**.

---

<div align="center">

### `MARKET DATA`

↓

### `STATISTICAL MODEL`

↓

### `10,000 PORTFOLIOS`

↓

### `EFFICIENT FRONTIER`

↓

### `OPTIMIZATION`

↓

### `PORTFOLIO ALLOCATION`

</div>

---

# ◈ Inside OptiVest

<table>
<tr>
<td width="50%" valign="top">

### 01 — Portfolio Optimization

Mean-variance optimization evaluates possible asset allocations based on their expected return and risk.

</td>

<td width="50%" valign="top">

### 02 — Monte Carlo Engine

**10,000 simulated portfolios** create a large risk-return landscape from which efficient portfolios can be identified.

</td>
</tr>

<tr>
<td width="50%" valign="top">

### 03 — Efficient Frontier

The system visualizes the relationship between portfolio risk and expected return to identify efficient allocations.

</td>

<td width="50%" valign="top">

### 04 — Maximum Sharpe

`scipy.optimize` searches for the allocation that maximizes the modeled Sharpe ratio.

</td>
</tr>

<tr>
<td width="50%" valign="top">

### 05 — Minimum Volatility

The optimization engine searches for the portfolio allocation with the lowest modeled volatility.

</td>

<td width="50%" valign="top">

### 06 — Risk Intelligence

Risk preferences are mapped to portfolio allocations to make the mathematical analysis easier to interpret.

</td>
</tr>
</table>

---

# ◉ The Engine

<div align="center">

```text
                     HISTORICAL PRICES
                            │
                            ▼
                     DAILY RETURNS
                            │
                            ▼
                    ANNUALIZED RETURNS
                            │
                            ▼
                    COVARIANCE MATRIX
                            │
                            ▼
              ┌──────────────────────────┐
              │     MONTE CARLO ENGINE   │
              │                          │
              │    10,000 PORTFOLIOS     │
              └────────────┬─────────────┘
                           │
                           ▼
                    RISK / RETURN CLOUD
                           │
                           ▼
                   EFFICIENT FRONTIER
                           │
                ┌──────────┴──────────┐
                ▼                     ▼
          MAXIMUM SHARPE        MINIMUM VOLATILITY
                │                     │
                └──────────┬──────────┘
                           ▼
                    RISK PREFERENCE
                           │
                           ▼
                   FINAL ALLOCATION
```

</div>

---

# ◌ The Mathematics

OptiVest is powered by **Modern Portfolio Theory**.

For a portfolio with asset weights:

$$
w_1,w_2,\ldots,w_n
$$

the expected portfolio return is:

$$
E(R_p)=\sum_i w_iE(R_i)
$$

Portfolio variance:

$$
\sigma_p^2=w^T\Sigma w
$$

Portfolio volatility:

$$
\sigma_p=\sqrt{w^T\Sigma w}
$$

And the Sharpe Ratio:

$$
S=\frac{R_p-R_f}{\sigma_p}
$$

The optimization engine uses these relationships to search the portfolio space for mathematically significant allocations.

---

# ⟡ From Data to Decision

<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=18&duration=1800&pause=500&color=7C3AED&center=true&vCenter=true&width=700&lines=FETCH+DATA;CALCULATE+RETURNS;BUILD+COVARIANCE+MATRIX;SIMULATE+10%2C000+PORTFOLIOS;BUILD+EFFICIENT+FRONTIER;OPTIMIZE;GENERATE+ALLOCATION" alt="Pipeline" />

</div>

---

# ◇ Product Experience

<div align="center">

### **A quantitative engine behind a clean financial interface.**

<br>

<!-- Add your real screenshots here -->

<img src="docs/dashboard.png" width="92%" alt="OptiVest Dashboard"/>

<br><br>

<table>
<tr>
<td width="50%">

<img src="docs/optimization.png" width="100%" alt="Portfolio Optimization"/>

</td>
<td width="50%">

<img src="docs/allocation.png" width="100%" alt="Portfolio Allocation"/>

</td>
</tr>
</table>

</div>

---

# ⌁ Architecture

<div align="center">

```text
                         ┌─────────────────────┐
                         │      OPTIVEST       │
                         │      FRONTEND       │
                         │                     │
                         │ React 19            │
                         │ Vite                │
                         │ Tailwind CSS         │
                         │ Recharts             │
                         └──────────┬──────────┘
                                    │
                               REST API
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │       FASTAPI       │
                         │       BACKEND       │
                         │                     │
                         │ Market Data         │
                         │ MPT Engine          │
                         │ Optimization        │
                         │ PDF Generation      │
                         └──────────┬──────────┘
                                    │
                 ┌──────────────────┼──────────────────┐
                 ▼                  ▼                  ▼
           Yahoo Finance         NumPy              SciPy
             yfinance            Pandas           Optimizer
                 │
                 ▼
          Historical Prices
```

</div>

---

# ⌂ Technology

<div align="center">

### FRONTEND

`React 19` · `Vite` · `Tailwind CSS` · `Recharts` · `Axios` · `Framer Motion` · `Lucide`

### BACKEND

`FastAPI` · `Python` · `Pandas` · `NumPy` · `SciPy` · `Scikit-learn` · `yfinance`

### OPTIMIZATION

`Modern Portfolio Theory` · `Mean-Variance Optimization` · `Monte Carlo Simulation` · `SLSQP`

</div>

---

# ◇ Data Resilience

External market-data APIs can fail.

OptiVest was designed so that the **demo does not collapse when market data becomes temporarily unavailable**.

```text
                    MARKET DATA REQUEST
                           │
                           ▼
                     YAHOO FINANCE
                           │
                  ┌────────┴────────┐
                  │                 │
               SUCCESS            FAILURE
                  │                 │
                  ▼                 ▼
             LIVE DATA        SYNTHETIC DATA
                  │                 │
                  └────────┬────────┘
                           ▼
                    MPT ENGINE
                           │
                           ▼
                       OPTIVEST
```

When fallback data is active, the backend exposes:

```json
{
  "is_simulated_data": true
}
```

The interface surfaces that state instead of silently presenting simulated data as live market information.

---

# ◇ Live

<div align="center">

<a href="https://optivest-psi.vercel.app/">

<img src="https://img.shields.io/badge/OPEN%20OPTIVEST%20↗-7C3AED?style=for-the-badge&labelColor=111111" />

</a>

<br><br>

**optivest-psi.vercel.app**

</div>

---

# 🏆 01 — HACKATHON

<div align="center">

<img src="https://img.shields.io/badge/1ST%20PRIZE-F5B942?style=for-the-badge&labelColor=111111" />

<br><br>

### **CENTRE OF EXCELLENCE HACKATHON**

**Kongu Engineering College**

<br>

OptiVest was developed and presented as a collaborative four-member project and was awarded **1st Prize** at the Centre of Excellence Hackathon.

</div>

---

# ◎ The Team

<div align="center">

## **FOUR MINDS. ONE PRODUCT.**

<br>

<table>
<tr>

<td align="center" width="25%">

### **NIRANJAN G**

<br>

`TEAM MEMBER`

</td>

<td align="center" width="25%">

### **NIRMAL KUMAR V**

<br>

`TEAM MEMBER`

</td>

<td align="center" width="25%">

### **NITHISH**

<br>

`TEAM MEMBER`

</td>

<td align="center" width="25%">

### **PRANESH DEEPAN**

<br>

`TEAM MEMBER`

</td>

</tr>
</table>

<br>

### **Equal Contribution**

All four members contributed equally across the project — from **ideation and architecture to engineering, optimization, interface design, testing and presentation.**

</div>

---

<div align="center">

<br><br>

# OPTIVEST

### **Risk isn't a number.**

### **It's a relationship between assets.**

<br>

**Analyze · Optimize · Understand**

<br>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=13&duration=3000&pause=1000&color=777777&center=true&vCenter=true&width=600&lines=Built+for+the+CoE+Hackathon.;Built+by+Niranjan+%C2%B7+Nirmal+%C2%B7+Nithish+%C2%B7+Pranesh." alt="Team" />

</div>

<br>

---

<div align="center">

<sub>OptiVest · Portfolio Risk & Return Intelligence</sub>

</div>
