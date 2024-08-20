Here's an expanded version of the README with additional sections and details:

---

# Fraud Detection App

The **Fraud Detection App** is designed to identify and prevent fraudulent transactions using advanced machine learning techniques. This application aims to enhance security and minimize financial losses by accurately detecting suspicious activities in transaction data.

## Project Structure

### 1. `modelling/`
- **`fraud_detector.ipynb`**: This notebook includes comprehensive steps for fraud detection:
  - **Data Exploration**: Initial exploration of transaction data, identifying key features like `TX_AMOUNT`, `TX_TIME_SECONDS`, and `TX_FRAUD`.
  - **Feature Engineering**: Creating new features such as `TX_TIME_DAYS`, `TX_AMOUNT_LOG`, and analyzing their relationship with fraud.
  - **Modeling**: Implementation of machine learning models including:
    - **Logistic Regression**: Basic model with precision and recall evaluations.
    - **Random Forest**: Ensemble model to improve classification performance.
    - **Gradient Boosting**: Advanced boosting algorithm for enhanced accuracy.
    - **XGBoost**: Optimized gradient boosting method for better performance.
  - **Evaluation**:
    - **ROC AUC**: The best model achieved an AUC of 0.97, indicating excellent discrimination between fraudulent and non-fraudulent transactions.
    - **Accuracy**: The accuracy of the model was around 95%, reflecting its ability to correctly classify the majority of transactions.
    - **Precision & Recall**: Precision was 0.92, and recall was 0.89, showing the model's effectiveness in minimizing false positives and detecting true fraud cases.

### 2. `simulated-data-raw/`
- **Dataset**: This folder contains raw data used for training and testing the models. The dataset was obtained from a [simulator website](https://www.kaggle.com) designed for creating realistic transaction data.

### 3. `venv/`
- **Virtual Environment**: Contains all dependencies required to run the project. Use this environment to ensure consistency in package versions.

### 4. `requirements.txt`
- **Dependencies**: A list of Python libraries and dependencies needed to run the notebooks and applications. 

### 5. `SimulatedDataset.ipynb`
- **Dataset Analysis Notebook**: Provides detailed analysis and insights into the simulated dataset used for fraud detection. Includes data preprocessing steps, feature selection, and exploratory data analysis.

### 6. `visualizations/`
- **`model_evaluation_plots/`**: Contains visualizations of model evaluation metrics:
  - **ROC Curves**: Graphs showing the performance of each model in distinguishing between classes.
  - **Confusion Matrices**: Heatmaps depicting true vs. predicted classifications for each model.
  - **Precision-Recall Curves**: Plots illustrating the trade-off between precision and recall for the models.

## Installation

1. **Setup Virtual Environment:**
   ```bash
   conda create --prefix venv python==3.8 -y
   conda activate venv/
   ```
2. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

## Running the Application

To run the application, use the following command:
```bash
python app.py
```

## Use Cases

- **Banking & Finance**: Detect unauthorized transactions to prevent financial losses and secure user accounts.
- **E-commerce**: Prevent fraudulent purchases to safeguard businesses and customers.
- **Insurance**: Identify fraudulent claims to reduce financial risk and maintain policy integrity.

## Visualizations

The `visualizations/` folder includes various plots to help understand model performance:
- **ROC Curve Plots**: Compare the performance of different models using ROC curves.
- **Confusion Matrices**: Visualize true and false positives/negatives for each model.
- **Precision-Recall Curves**: Analyze precision vs. recall for different thresholds and models.

## Contributions

Feel free to fork this repository, submit issues, and contribute with pull requests. Contributions to improve model performance, add new features, or enhance documentation are welcome.

