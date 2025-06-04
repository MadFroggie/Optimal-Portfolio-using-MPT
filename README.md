# 📊 Portfolio Optimization using Modern Portfolio Theory (Markowitz Model)

This project demonstrates the implementation of **Modern Portfolio Theory (MPT)** using historical stock data. It helps an investor construct an optimal portfolio that maximizes expected return for a given level of risk, or equivalently, minimizes risk for a given level of return.

---

## 📚 Theory - Modern Portfolio Theory

Modern Portfolio Theory (MPT), introduced by **Harry Markowitz**, provides a mathematical framework for assembling a portfolio of assets to maximize expected return based on a given level of market risk.

### ⚙️ Key Concepts and Formulas

#### 1. **Portfolio Return**
\[
R_p = \sum_{i=1}^{n} w_i \cdot R_i
\]
Where:
- \( R_p \) = Expected portfolio return
- \( w_i \) = Weight of asset \( i \)
- \( R_i \) = Expected return of asset \( i \)

#### 2. **Portfolio Volatility (Standard Deviation)**
\[
\sigma_p = \sqrt{w^T \Sigma w}
\]
Where:
- \( \Sigma \) = Covariance matrix of asset returns
- \( w \) = Weight vector

#### 3. **Sharpe Ratio**
\[
\text{Sharpe Ratio} = \frac{R_p - R_f}{\sigma_p}
\]
Where:
- \( R_f \) = Risk-free rate (assumed 0 in this model)

---

## 🧪 Data & Dependencies

### ✅ Libraries Used
- `numpy`
- `pandas`
- `matplotlib`, `seaborn`
- `yfinance` *(for downloading stock data)*

### 📁 Data Files
The following `.csv` files must be in the project folder:
- `KEC.csv`
- `mazgon.csv`
- `Reliance.csv`
- `Tatamotors.csv`

Ensure these files have at least:
- `'Date '` (note the trailing space) column
- `'vwap '` (trailing space again) column for price data

---

## 🧩 Code Structure

### 1. **Data Import and Preparation**
```python
KEC = pd.read_csv('KEC.csv')
mazagon = pd.read_csv('mazgon.csv')
reliance = pd.read_csv('Reliance.csv')
tata_motors = pd.read_csv('Tatamotors.csv')
