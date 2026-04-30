# Machine Learning Exercises Repository

## Overview

This repository contains a collection of Jupyter notebooks, datasets, and supporting Python scripts that demonstrate core concepts in **machine learning** (both classification and regression). The exercises are organized by topic and difficulty level, making it easy for students, educators, and practitioners to explore:

- **Classification** (logistic regression, precision‑recall analysis, etc.)
- **Regression** (linear regression, regularization, one‑hot encoding, multiple variables, etc.)
- **Optimization** (gradient descent implementations)
- **Model evaluation** (train/test splits, performance metrics)

Each sub‑directory includes:

- An `assignment.ipynb` notebook that walks through the problem statement, data preprocessing, model building, and interpretation of results.
- Associated CSV/Excel data files used in the notebooks.
- Occasionally, helper Python scripts (e.g., `gd.py`, `gradient_descent.py`).

The goal is to provide a hands‑on learning resource that can be run locally with minimal setup.

## Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/your‑username/ML-Exercises.git
   cd ML-Exercises
   ```

2. **Create a virtual environment (optional but recommended)**
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows use `venv\Scripts\activate`
   ```

3. **Install required Python packages**
   The notebooks rely on common data‑science libraries. Install them with:
   ```bash
   pip install -r requirements.txt
   ```
   > **Note:** A `requirements.txt` file is not currently present. You can generate one based on the imports in the notebooks, typically including:
   > `numpy`, `pandas`, `scikit-learn`, `matplotlib`, `seaborn`, `jupyter`.

4. **Launch Jupyter Notebook / JupyterLab**
   ```bash
   jupyter notebook   # or `jupyter lab`
   ```
   Open the desired `*.ipynb` file and run the cells sequentially.

## Usage Examples

Below are quick examples of how to run a specific exercise.

### Example: Logistic Regression Classification

```bash
cd ML_classification_LogisticRegression_resources
jupyter notebook logistic_regression_single_class.ipynb
```
The notebook will:
1. Load the `car_ownership.csv` dataset.
2. Perform exploratory data analysis.
3. Train a logistic regression model using scikit‑learn.
4. Visualize decision boundaries and evaluate performance.

### Example: Gradient Descent Implementation

```bash
cd gradient_descent
python gd.py
```
`gd.py` contains a simple implementation of gradient descent on a synthetic dataset. Running the script prints the optimized parameters and plots the convergence curve.

## Contributing Guidelines

Contributions are welcome! Follow these steps to propose improvements:

1. **Fork the repository** on GitHub.
2. **Create a new branch** for your feature or bug‑fix:
   ```bash
   git checkout -b feature/your‑feature-name
   ```
3. **Make your changes** – add notebooks, improve existing ones, fix typos, or add documentation.
4. **Add tests** (if applicable) and ensure existing notebooks run without errors.
5. **Commit your changes** with a clear message:
   ```bash
   git commit -m "Add XYZ feature / Fix ABC issue"
   ```
6. **Push the branch** to your fork and open a Pull Request (PR) against the `main` branch of the upstream repository.
7. **PR Checklist**:
   - [ ] Title follows the pattern `feat:`, `fix:`, or `docs:`.
   - [ ] Description explains the change and any relevant context.
   - [ ] All notebooks run from start to finish.
   - [ ] Updated `README.md` or other docs if needed.

## License

This project is licensed under the **MIT License** – see the `LICENSE` file for details.

---

*Happy learning!*