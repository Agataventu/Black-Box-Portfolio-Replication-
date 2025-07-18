# Black-Box-Portfolio-Replication-
# Portfolio Replication Strategy

## Overview
This project focuses on replicating the performance of a **black-box portfolio** (e.g., a hedge fund or proprietary index) using **only historical return data**, without knowing the actual assets or weights inside the portfolio. The goal is to build a **replicating portfolio** using liquid and transparent instruments (e.g., futures, indices), closely tracking the target portfolio’s returns while maintaining **interpretability** and **tractability**.

## Objectives

- Reproduce the return behavior of a target portfolio using observable financial instruments.
- Explore regression-based techniques to estimate asset exposures.
- Ensure simplicity, interpretability, and low turnover in the replicating portfolio.

## Methods Used

- **Linear regression** to estimate portfolio exposures.
- **LASSO regression** (L1 regularization) to reduce overfitting and penalize excessive complexity.
- **Non-negative least squares** to constrain weights to be ≥ 0 (realistic long-only strategies).
- **Turnover control** via regularization to minimize rebalancing frequency and trading costs.

## Files
├── Dataset_PortfolioReplicaStrategy.xlsx # Historical weekly returns for target and factors
├── Portfolio_Replica.ipynb # Baseline portfolio replication via regression --> Enhanced model with regularization and constraints
├── README.md # Project summary and documentation

## Dataset

- **Period**: Weekly data from 2007 to 2021
- **Target**: Global Hedge Fund Index (returns are known, composition is not)
- **Factors**: MSCI indices, global bond aggregates, and key futures contracts

## Key Concepts
- **Portfolio cloning**: Reverse-engineering the hidden composition of a portfolio using observed returns.
- **Use cases**:
  - Hedge fund replication with lower fees
  - UCITS-compliant product development
  - Illiquid index tracking
  - Risk factor decomposition
- **Futures-based replication**: Mimicking portfolio behavior with minimal capital commitment via futures contracts.

**Autors**
Brignoli Ettore, Capoferri Luca, Untila Denis, Venturi Agata

*This project was developed for academic purposes as part of the **Fintech** course at **Politecnico di Milano (PoliMI)**.
