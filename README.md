# 🌳 Non-linear Modeling & Tree-Based Ensemble Labs

[![GitHub Stars](https://img.shields.io/github/stars/wajason/ISLR-Ch7-8-Non-linear-and-tree-models-Labs?style=for-the-badge&logo=github&color=6699CC)](https://github.com/wajason/ISLR-Ch7-8-Non-linear-and-tree-models-Labs/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/wajason/ISLR-Ch7-8-Non-linear-and-tree-models-Labs?style=for-the-badge&logo=github&color=6699CC)](https://github.com/wajason/ISLR-Ch7-8-Non-linear-and-tree-models-Labs/network/members)
[![Issues](https://img.shields.io/github/issues/wajason/ISLR-Ch7-8-Non-linear-and-tree-models-Labs?style=for-the-badge&color=6699CC)](https://github.com/wajason/ISLR-Ch7-8-Non-linear-and-tree-models-Labs/issues)
[![License](https://img.shields.io/badge/License-MIT-6699CC?style=for-the-badge)](./LICENSE)

This repository contains a comprehensive R implementation and detailed analysis of the code presented in **Chapter 7.8 (Non-linear Modeling)** and **Chapter 8.3 (Decision Trees)** of *An Introduction to Statistical Learning* (James et al., 2021).

The aim is to provide a clear, step-by-step tutorial on fitting non-linear and non-parametric models, including the most popular tree-based ensemble learning strategies, using the `Wage`, `Carseats`, and `Boston` datasets.

---

## ✨ Key Features & Highlights

This tutorial goes beyond simply repeating the code by including:

* **Non-linear Modeling (Ch 7):**
    * **Regression Splines:** Implementing B-Splines ($bs()$) and Natural Splines ($ns()$) to fit flexible curves.
    * **Smoothing Methods:** Using Local Regression ($loess()$) and Smoothing Splines ($smooth.spline()$) (with cross-validation for parameter selection).
    * **Generalized Additive Models (GAMs):** Fitting GAMs with smoothing splines ($s()$), local regression ($lo()$) , and applying GAMs to Logistic Regression ($family = binomial$).

* **Decision Trees (Ch 8):**
    * **Classification & Regression Trees:** Fitting trees using the `tree` package and pruning based on cross-validation (misclassification error or RSS).
    * **Bagging & Random Forests:** Implementing Bagging (setting $mtry = p$) and Random Forests for regression, including variable importance analysis.
    * **Boosting (GBM):** Using Gradient Boosting for regression , featuring partial dependence plots and shrinkage parameter tuning.
    * **BART:** Implementing **Bayesian Additive Regression Trees** ($gbart()$) for state-of-the-art non-parametric regression.

---

## 📂 Repository Structure

| File | Description |
| :--- | :--- |
| `Non-linear and tree models Tutorials.pdf` | **The fully rendered tutorial.** Contains all R code, output, plots (Splines, GAMs, Tree structures, Importance plots), and detailed personal commentary/analysis. |
| `README.md` | Project overview, links, and reproduction instructions. |

---

## 🛠️ Data Source & Reproduction

### Data Source
All data and primary code structure are derived from:
* **Book:** *An Introduction to Statistical Learning with Applications in R* (ISLR).
* **Authors:** Gareth James, Daniela Witten, Trevor Hastie, Robert Tibshirani (2021).
* **Key Datasets:**
    * `Wage`: Used for non-linear models (Polynomials, Splines, GAMs).
    * `Carseats`: Used for Classification Trees.
    * `Boston`: Used for Regression Trees, Bagging, Random Forests, Boosting, and BART.

### Required R Packages
To recreate the analysis, you will need the following packages:
* `ISLR2` (Datasets) 
* `splines` (For $bs()$ and $ns()$ basis functions)
* `gam` (For Generalized Additive Models) 
* `akima` (For 2D smooth plots in GAMs) 
* `tree` (For Decision Trees) 
* `randomForest` (For Bagging & Random Forests) 
* `gbm` (For Gradient Boosting Machines) 
* `BART` (For Bayesian Additive Regression Trees)

### How to Reproduce
1.  **Clone** this repository:
    ```bash
    git clone [https://github.com/wajason/ISLR-Ch7-8-Non-linear-and-tree-models-Labs.git](https://github.com/wajason/ISLR-Ch7-8-Non-linear-and-tree-models-Labs.git)
    ```
2.  **Download** the PDF file to view the full annotated code.
3.  Install the required packages in R:
    ```r
    install.packages(c("ISLR2", "splines", "gam", "akima", "tree", "randomForest", "gbm", "BART"))
    ```
4.  Copy the code segments from the tutorial (`Non-linear and tree models Tutorials.pdf`) into your R environment to execute.
