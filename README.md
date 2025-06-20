# 🧠 ML Basics Showcase: Logistic Regression & MLP Classifiers

This project is to demonstrate foundational image classification workflows using Logistic Regression and Multi-Layer Perceptron (MLP) on benchmark datasets like Fashion-MNIST and CIFAR-10. It is designed as an introduction to deep learning and to highlight key concepts of machine learning algorithms through hands-on training, evaluation, and visualization. It also visualizes the most significant weights/inputs for logistic regression and maps out the loss curve to understand model convergence.

---

## 📁 Project Structure

```bash
intro-to-ml-basics/
├── scripts/              # Reusable Python modules
│   ├── dataset_loader.py
│   ├── dying_neuron_test.py
│   ├── loss_surface_plotting.py
│   └── model_loader.py
├── notebooks/            # Experiments and visualizations
│   ├── logistic_regression_performance.ipynb
│   └── classification_with_MLP.ipynb
├── requirements.txt
├── config.yaml
└── README.md
```

---

## 📌 Objectives

* Implement logistic regression and MLP from scratch using Tensorflow
* Train on Fashion-MNIST/CIFAR datasets
* Visualize training and validation performance
* Understand underfitting vs overfitting, and the bias-variance tradeoff
* Apply techniques like initialization, regularization and dropout

---

## 🛠️ Models Implemented

| Model               | Dataset       | Key Features                              |
| ------------------- | ------------- | ----------------------------------------- |
| Logistic Regression |  FMNIST       | Linear classifier with Softmax activation |
| MLP (single layer)  | FMNIST, CIFAR | ReLU, Softmax, Early Stopping             |
| MLP (3 layers)      | FMNIST, CIFAR | He Normal initialization, Leaky ReLU, Dropout, Softmax, L2 regularization       |

---

## 📊 Results

Here are the Performance metrics and training/validation curves:

| Model               | Dataset | Accuracy | Notes               |
| ------------------- | ------- | -------- | ------------------- |
| Logistic Regression (w\o Regularization) | FMNIST | \~84.59% | Simple linear model |
| Logistic Regression (l2 Regularization & Early callback) | FMNIST  | \~81.92% | Impose Prior Bias & Stop Overfitting through Early Stopping|
| MLP (1-layer)       | FMNIST  | \~88.26% | Better nonlinearity |
|                      | CIFAR   | \~46.95% | Underfit model      |
| MLP (3-layers & Dropout)       | FMNIST  | \~88.46% | Similar Performance |
|                 | CIFAR   | \~57.34% | Struggle to fit data|

> 📈 Training & validation accuracy, most relevant pixels, and loss curves are visualized in the notebooks under `/notebooks`.

---

## 🔍 Key Takeaways

* Logistic regression can perform relatively well on simpler datasets like FMNIST.
* MLPs can model more complex decision boundaries with hidden layers but still struggles with complex data like RGB images in CIFAR-10.
* Proper parameter initialization helps avoid vanishing and exploding gradients.
* Dropout and L2 regularization are helpful in reducing overfitting, especially for deeper models.
* The concept of Bias-Variance trade-off is also explored for the deep MLP model.

---

## ⚙ Trainable Model Params

* The shallow MLP model has 604938 trainable params.
* and, The deeper MLP model has 3071754 trainable params.
* Higher number of parameter indicates increased model capacity.

## 🚀 Setup Instructions

### 1. Clone the repository

```bash
git https://github.com/Salekin-13/intro-to-ml-basics.git
cd intro-to-ml-basics
```

### 2. Set up environment

```bash
pip install -r requirements.txt
```

---

## 📎 Notes

* Built with educational clarity in mind — every function and model is well-commented and structured
* Easy to extend with CNN or other datasets
* No external training libraries used — just Tensorflow and NumPy

---

## 💡 Future Work

* Add CNN-based classifier
* Add noise to input images and measure the change in accuracy

---

## 🙋‍♀️ Author

Made by \[Sumaiya Salekin]
Inspired by classic ML fundamentals 🌱

## 📚 References

- MLU-Explain. *Bias-Variance Tradeoff*. [https://mlu-explain.github.io/bias-variance/](https://mlu-explain.github.io/bias-variance/)
- Zhang, A., Lipton, Z. C., Li, M., & Smola, A. J. *Dive into Deep Learning*. [https://d2l.ai](https://d2l.ai)

