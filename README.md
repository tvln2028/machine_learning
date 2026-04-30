# Machine Learning Exercises Repository

## Overview

This repository contains a collection of Jupyter notebooks, datasets, and supporting Python scripts that cover various machine learning topics ranging from basic classification and regression exercises to more advanced concepts such as regularization, one‑hot encoding, and gradient descent. The material is organized into separate folders for each exercise or tutorial, making it easy to explore and run the examples independently.

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your‑username/your‑repo‑name.git
   cd your-repo-name
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
   If a `requirements.txt` file is not present, you can install the most common dependencies manually:
   ```bash
   pip install numpy pandas matplotlib scikit-learn jupyter
   ```

4. **Start Jupyter Notebook**
   ```bash
   jupyter notebook
   ```
   Then navigate to the folder of the exercise you want to run.

## Usage Examples

Below are a few quick examples of how to run the notebooks:

- **Classification Exercise** – `ML_Classification_Exercise1/assignment.ipynb`
  - Loads the `social_network_ads.csv` dataset and demonstrates logistic regression for binary classification.

- **Regression Exercise** – `ML_Regression_Exercise1/assignment.ipynb`
  - Uses the `weather_data.csv` dataset to fit a simple linear regression model.

- **Regularization Tutorial** – `ML_Regression_L1L2Regularization_resources/L1_L2_regularization_tutorial.ipynb`
  - Shows how L1 (Lasso) and L2 (Ridge) regularization affect model coefficients.

You can open any notebook in Jupyter, run the cells sequentially, and modify the code to experiment with different parameters.

## Contributing Guidelines

We welcome contributions! Please follow these steps:

1. **Fork the repository** and clone your fork.
2. **Create a new branch** for your feature or bug‑fix.
   ```bash
   git checkout -b my-feature-branch
   ```
3. **Make your changes** – add notebooks, datasets, or improve existing code.
4. **Write or update documentation** – ensure that any new notebooks have clear headings and comments.
5. **Run the notebooks** to verify they execute without errors.
6. **Commit your changes** with a descriptive message.
7. **Push to your fork** and open a Pull Request targeting the `main` branch.

Please adhere to the following style guidelines:
- Use **PEP 8** for Python code.
- Keep notebook cells short and focused.
- Include markdown cells that explain the purpose of each step.
- Update the `README.md` if you add new exercises or change the project structure.

## License

This project is licensed under the **MIT License**. See the `LICENSE` file for full details.

---

*Happy learning!*