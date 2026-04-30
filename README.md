# Machine Learning Exercises & Resources Repository

## 📚 Overview

This repository is a curated collection of **machine learning (ML) exercises**, **Jupyter notebooks**, and **supporting datasets** covering a variety of topics:

- **Classification** – logistic regression, precision‑recall analysis, social‑network ads classification, etc.
- **Regression** – linear regression, multiple linear regression, L1/L2 regularization, one‑hot encoding, GDP forecasting, and more.
- **Utilities** – gradient descent implementation, train‑test split examples.

Each exercise is self‑contained: the notebook (`*.ipynb`) demonstrates the theory, the code, and the results, while the accompanying CSV/Excel files provide the data.

The goal is to serve as a **learning resource** for students, instructors, and anyone looking to practice core ML concepts with real‑world data.

---

## ⚙️ Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your‑username/ML‑Exercises.git
   cd ML‑Exercises
   ```

2. **Create a virtual environment** (optional but recommended)
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. **Install the required Python packages**
   ```bash
   pip install -r requirements.txt
   ```
   > **Note**: If a `requirements.txt` file is not present, you can install the most common packages used across the notebooks:
   ```bash
   pip install numpy pandas matplotlib scikit-learn seaborn jupyter
   ```

4. **Launch Jupyter Notebook / JupyterLab**
   ```bash
   jupyter notebook   # or jupyter lab
   ```
   Open any notebook inside the sub‑folders to explore the exercises.

---

## 🚀 Usage Examples

Below are quick examples of how to run a few representative notebooks.

### 1. Classification – Logistic Regression

```bash
cd ML_classification_LogisticRegression_resources
jupyter notebook logistic_regression_single_class.ipynb
```
The notebook walks through loading `car_ownership.csv`, visualising the data, training a logistic regression model, and evaluating performance.

### 2. Regression – Linear Regression (Single Variable)

```bash
cd ML_Regression_LinearRegression_resources
jupyter notebook linear_regression_single_variable.ipynb
```
It demonstrates fitting a simple linear model to `home_prices.csv` and visualising the regression line.

### 3. Gradient Descent Implementation

```bash
cd gradient_descent
python gd.py
```
The script runs a basic gradient descent optimizer on a synthetic dataset and prints the learned parameters.

---

## 🤝 Contributing

Contributions are welcome! Whether you want to add new exercises, improve existing notebooks, or fix bugs, please follow these steps:

1. **Fork the repository** and clone your fork.
2. **Create a new branch** for your contribution:
   ```bash
   git checkout -b my‑feature‑branch
   ```
3. **Make your changes** – add notebooks, update code, improve documentation, etc.
4. **Ensure the repository builds** (run notebooks, lint Python files, etc.).
5. **Commit your changes** with a clear message:
   ```bash
   git commit -m "Add <description of change>"
   ```
6. **Push to your fork** and open a **Pull Request** against the `main` branch.
   - Provide a concise PR title (e.g., `Add Lasso regression exercise`).
   - Include a description of what was added/changed and why.

### Code Style & Guidelines

- Follow **PEP 8** for Python code.
- Use **Markdown** cells in notebooks to explain the theory and steps.
- Keep notebooks **executable from start to finish** (no hidden state).
- Update the `README.md` if you add a new top‑level exercise folder.

---

## 📄 License

This repository is licensed under the **MIT License** – see the `LICENSE` file for details.

---

## 📞 Contact

For questions or suggestions, feel free to open an issue or contact the repository maintainer.
