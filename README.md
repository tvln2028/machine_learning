# Machine Learning Exercises Repository

## Overview

This repository contains a collection of educational resources, Jupyter notebooks, datasets, and Python scripts that demonstrate fundamental concepts in **machine learning**, **regression**, and **classification**.  The material is organized by topic (e.g., classification, regression, gradient descent) and is intended for students, instructors, and anyone looking to get hands‑on experience with classic ML algorithms.

## Directory Structure

```
.
├── ML_Classification_Exercise1/                # Intro to classification (logistic regression)
├── ML_Classification_PrecisionRecall_resources/ # Precision‑Recall notebooks & data
├── ML_Regression_Exercise1/ … 5/               # Regression exercises (simple, multiple, L1/L2, one‑hot)
├── ML_Regression_L1L2Regularization_resources/ # L1/L2 regularization tutorial & data
├── ML_Regression_LinearRegression_resources/   # Simple linear regression examples
├── ML_Regression_MultipleLinearRegression_resources/ # Multiple linear regression examples
├── ML_Regression_OneHotEncoding_resources/    # One‑hot encoding tutorial
├── ML_classification_LogisticRegression_resources/ # Logistic regression data & notebook
├── gradient_descent/                           # Gradient‑descent implementation & data
│   ├── gd.py                                   # Core gradient‑descent script
│   └── home_prices.csv                         # Sample dataset used by gd.py
├── train_test/                                 # Miscellaneous notebook for train‑test split
└── docs/                                       # **New** – documentation files (API reference, etc.)
```

## Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your‑username>/<repo‑name>.git
   cd <repo‑name>
   ```

2. **Create a virtual environment (recommended)**
   ```bash
   python -m venv venv
   source venv/bin/activate   # on Windows use `venv\Scripts\activate`
   ```

3. **Install required packages**
   The notebooks use the common scientific stack.  Install it via:
   ```bash
   pip install -r requirements.txt   # (if a requirements file is added later)
   # Or install manually:
   pip install pandas numpy matplotlib scikit-learn jupyter
   ```

4. **Explore the notebooks**
   Launch Jupyter to view the exercises:
   ```bash
   jupyter notebook
   ```
   Open any folder (e.g., `ML_Regression_Exercise1/assignment.ipynb`) and run the cells.

## Running the Gradient‑Descent Example

The `gradient_descent/gd.py` script implements a simple gradient‑descent optimizer for a univariate linear regression problem.  It scales the data, performs gradient descent, and then rescales the learned parameters back to the original units.

```bash
python gradient_descent/gd.py
```

The script reads `gradient_descent/home_prices.csv`, fits a line to predict house price from area, and prints the final slope (`m`) and intercept (`b`).  You can also import the `gradient_descent` function in your own code:

```python
from gradient_descent.gd import gradient_descent
import pandas as pd

df = pd.read_csv('gradient_descent/home_prices.csv')
X = df['area_sqr_ft'].to_numpy()
Y = df['price_lakhs'].to_numpy()
intercept, slope = gradient_descent(X, Y, lr=0.05, epochs=5000)
print(intercept, slope)
```

## API Reference

A concise API reference for the public functions is provided in **`docs/API.md`**.  It describes the `gradient_descent` function, its parameters, return values, and a short example.

## Contributing

Contributions are welcome!  If you would like to add new exercises, improve existing notebooks, or enhance the documentation, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b my‑feature`).
3. Make your changes.
4. Ensure notebooks run without errors.
5. Submit a pull request describing the changes.

## License

This collection of educational resources is released under the **MIT License**.  See the `LICENSE` file for details.

---

*Happy learning!*