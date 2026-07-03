# 🧠 Machine Learning Workshop

A collection of machine learning mini-projects covering regression, classification, and deep learning — built during a hands-on ML workshop.

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![scikit--learn](https://img.shields.io/badge/scikit--learn-ML%20Models-F7931E?logo=scikitlearn)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Keras-FF6F00?logo=tensorflow)
![Status](https://img.shields.io/badge/status-active-brightgreen)

---

## 📖 About

This repository brings together every project completed during the Machine Learning Workshop into a single, organized monorepo. It spans the core ML spectrum — a **regression** problem (house price prediction), a **classification** problem (loan approval prediction), and a **deep learning** problem (image classification with a CNN) — each demonstrating a full, practical ML workflow from raw data to a trained, evaluated model.

## 🗂️ Projects

| Project | Type | Description |
|---|---|---|
| [House Price Prediction](./HousePricePrediction) | Regression | Predicts housing prices from property features using a K-Nearest Neighbors Regressor. |
| [Loan Approval Prediction](./LoanApprovalPrediction) | Classification | Predicts loan approval status from applicant and financial data using Logistic Regression (with Decision Tree / Random Forest in progress). |
| [Image Classification](./ImageClassification) | Deep Learning | Classifies images into 10 categories using a CNN trained on CIFAR-10, with live prediction on custom uploaded images. |

## 📁 Repository Structure

```
Machine-Learning-Workshop/
├── HousePricePrediction/
│   └── README.md
├── LoanApprovalPrediction/
│   └── README.md
├── ImageClassification/
│   ├── README.md
│   ├── imageClassification_clean.ipynb
│   └── cnn_cifar10_model.keras
└── README.md
```

## 🚀 Getting Started

Clone the full repository:

```bash
git clone https://github.com/DuvvuLakshmiPrasanna/Machine-Learning-Workshop.git
cd Machine-Learning-Workshop
```

Each project folder is self-contained — `cd` into the one you're interested in and check its own `README.md` for setup and usage details specific to that project.

### Prerequisites

```bash
pip install pandas scikit-learn tensorflow ipywidgets numpy
```

- Python 3.9+
- Jupyter Notebook / JupyterLab (or Google Colab / Kaggle)

## 🧰 Tech Stack

| Category | Tools |
|---|---|
| Language | Python |
| Data Handling | Pandas, NumPy |
| Classical ML | scikit-learn (KNN, Logistic Regression, Decision Tree, Random Forest) |
| Deep Learning | TensorFlow / Keras (CNN) |
| Environment | Jupyter Notebook |

## 📊 Project Highlights

| Project | Model(s) | Key Metric |
|---|---|---|
| House Price Prediction | KNN Regressor | RMSE ≈ 1,449,751.66 |
| Loan Approval Prediction | Logistic Regression | Accuracy ≈ 78.33% |
| Image Classification | CNN (3 Conv layers) | Trained 10 epochs on CIFAR-10 |

## 🤝 Contributing

This is a personal workshop archive, but suggestions and improvements are welcome — feel free to open an issue or submit a pull request.

## 📄 License

This project is shared for educational purposes. Add a license file if you'd like to specify usage terms.

## 👤 Author

**Duvvu Lakshmi Prasanna**
[GitHub](https://github.com/DuvvuLakshmiPrasanna)
