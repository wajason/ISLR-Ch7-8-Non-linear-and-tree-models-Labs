# 🌳 Non-linear Modeling & Tree-Based Ensemble Labs

[![GitHub Stars](https://img.shields.io/github/stars/wajason/ISLR-Ch7-8-Non-linear-and-tree-models-Labs?style=for-the-badge&logo=github&color=6699CC)](https://github.com/wajason/ISLR-Ch7-8-Non-linear-and-tree-models-Labs/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/wajason/ISLR-Ch7-8-Non-linear-and-tree-models-Labs?style=for-the-badge&logo=github&color=6699CC)](https://github.com/wajason/ISLR-Ch7-8-Non-linear-and-tree-models-Labs/network/members)
[![Issues](https://img.shields.io/github/issues/wajason/ISLR-Ch7-8-Non-linear-and-tree-models-Labs?style=for-the-badge&color=6699CC)](https://github.com/wajason/ISLR-Ch7-8-Non-linear-and-tree-models-Labs/issues)
[![License](https://img.shields.io/badge/License-MIT-6699CC?style=for-the-badge)](./LICENSE)

[cite_start]This repository contains a comprehensive R implementation and detailed analysis of the code presented in **Chapter 7.8 (Non-linear Modeling)** and **Chapter 8.3 (Decision Trees)** of *An Introduction to Statistical Learning* (James et al., 2021)[cite: 2].

[cite_start]The aim is to provide a clear, step-by-step tutorial on fitting non-linear and non-parametric models, including the most popular tree-based ensemble learning strategies, using the `Wage`, `Carseats`, and `Boston` datasets[cite: 2].

---

## ✨ Key Features & Highlights

This tutorial goes beyond simply repeating the code by including:

* **Non-linear Modeling (Ch 7):**
    * [cite_start]**Regression Splines:** Implementing B-Splines ($bs()$) and Natural Splines ($ns()$) to fit flexible curves[cite: 238, 292].
    * [cite_start]**Smoothing Methods:** Using Local Regression ($loess()$) [cite: 361] [cite_start]and Smoothing Splines ($smooth.spline()$) (with cross-validation for parameter selection)[cite: 314, 316].
    * [cite_start]**Generalized Additive Models (GAMs):** Fitting GAMs with smoothing splines ($s()$), local regression ($lo()$) [cite: 417, 551][cite_start], and applying GAMs to Logistic Regression ($family = binomial$)[cite: 606, 613].

* **Decision Trees (Ch 8):**
    * [cite_start]**Classification & Regression Trees:** Fitting trees using the `tree` package and pruning based on cross-validation (misclassification error or RSS)[cite: 696, 828, 947].
    * [cite_start]**Bagging & Random Forests:** Implementing Bagging (setting $mtry = p$) [cite: 1055] [cite_start]and Random Forests [cite: 1098] [cite_start]for regression, including variable importance analysis[cite: 1107, 1109].
    * [cite_start]**Boosting (GBM):** Using Gradient Boosting for regression [cite: 1153][cite_start], featuring partial dependence plots [cite: 1181] [cite_start]and shrinkage parameter tuning[cite: 1213].
    * [cite_start]**BART:** Implementing **Bayesian Additive Regression Trees** ($gbart()$) for state-of-the-art non-parametric regression[cite: 1228, 1248].

---

## 📂 Repository Structure

| File | Description |
| :--- | :--- |
| `Non-linear and tree models Tutorials.pdf` | [cite_start]**The fully rendered tutorial.** Contains all R code, output, plots (Splines, GAMs, Tree structures, Importance plots), and detailed personal commentary/analysis[cite: 2]. |
| `README.md` | Project overview, links, and reproduction instructions. |

---

## 🛠️ Data Source & Reproduction

### Data Source
All data and primary code structure are derived from:
* [cite_start]**Book:** *An Introduction to Statistical Learning with Applications in R* (ISLR)[cite: 2].
* [cite_start]**Authors:** Gareth James, Daniela Witten, Trevor Hastie, Robert Tibshirani (2021)[cite: 2].
* **Key Datasets:**
    * [cite_start]`Wage`: Used for non-linear models (Polynomials, Splines, GAMs)[cite: 9, 13].
    * [cite_start]`Carseats`: Used for Classification Trees[cite: 699, 705].
    * [cite_start]`Boston`: Used for Regression Trees, Bagging, Random Forests, Boosting, and BART[cite: 945, 1054, 1155, 1234].

### Required R Packages
To recreate the analysis, you will need the following packages:
* [cite_start]`ISLR2` (Datasets) [cite: 698]
* [cite_start]`splines` (For $bs()$ and $ns()$ basis functions) [cite: 240]
* [cite_start]`gam` (For Generalized Additive Models) [cite: 415]
* [cite_start]`akima` (For 2D smooth plots in GAMs) [cite: 592]
* [cite_start]`tree` (For Decision Trees) [cite: 696]
* [cite_start]`randomForest` (For Bagging & Random Forests) [cite: 1051]
* [cite_start]`gbm` (For Gradient Boosting Machines) [cite: 1149]
* [cite_start]`BART` (For Bayesian Additive Regression Trees) [cite: 1231]

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
