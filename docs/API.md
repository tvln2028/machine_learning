# API Documentation

## gradient_descent.gradient_descent

```python
gradient_descent(x: np.ndarray, y: np.ndarray, lr: float = 0.1, epochs: int = 3000) -> Tuple[float, float]
```

### Description

Performs **gradient descent** to fit a simple linear regression model (y = m·x + b) on a single‑feature dataset. The function internally scales both the feature vector `x` and target vector `y` using Min‑Max scaling, runs the optimization, and finally rescales the learned parameters back to the original data space.

### Parameters

| Name | Type | Default | Description |
|------|------|---------|-------------|
| `x` | `np.ndarray` | – | 1‑D array of input feature values (e.g., house area). |
| `y` | `np.ndarray` | – | 1‑D array of target values (e.g., house price). |
| `lr` | `float` | `0.1` | Learning rate controlling the step size for each iteration. |
| `epochs` | `int` | `3000` | Number of gradient‑descent iterations.

### Returns

A tuple `(b_original, m_original)` where:
- `b_original` – Intercept of the fitted line in the original data scale.
- `m_original` – Slope of the fitted line in the original data scale.

### Example Usage

```python
import pandas as pd
from gradient_descent.gd import gradient_descent

# Load example data
df = pd.read_csv('gradient_descent/home_prices.csv')
X = df['area_sqr_ft'].to_numpy()
Y = df['price_lakhs'].to_numpy()

# Fit the model
intercept, slope = gradient_descent(X, Y, lr=0.05, epochs=5000)
print(f"Intercept: {intercept:.4f}, Slope: {slope:.4f}")
```

### Implementation Details

1. **Scaling** – Min‑Max scaling is applied to both `x` and `y` to improve numerical stability.
2. **Gradient Computation** – The gradients of the mean‑squared error loss with respect to `b` (intercept) and `m` (slope) are:
   - `db = -2 * mean(error)`
   - `dm = -2 * mean(error * x_scaled)`
3. **Parameter Update** – Parameters are updated using the standard gradient‑descent rule:
   - `b = b - lr * db`
   - `m = m - lr * dm`
4. **Rescaling** – After training, the learned parameters are transformed back to the original scale using the stored min/max values.

---

## Module Overview

- **File:** `gradient_descent/gd.py`
- **Exports:** `gradient_descent` (the core function) and a CLI entry point that reads `home_prices.csv` and prints the final model parameters.

---

*For any additional scripts or utilities added in the future, extend this API documentation accordingly.*