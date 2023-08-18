# Model-versioning-and-registration-with-MLFlow

## 1: MLOps with PyCaret and MLFlow

### Description
This code demonstrates the use of MLOps (Machine Learning Operations) by combining PyCaret and MLFlow to streamline the machine learning workflow. It showcases data loading, preprocessing, model selection, evaluation, and prediction using the PyCaret library, along with experiment tracking and model management using MLFlow.

### Code Explanation
#### Get Data: 
The dataset is loaded using PyCaret's get_data function.

#### Preprocessing: 
PyCaret's setup function is used to initialize the experiment. Data preprocessing is performed, and the target variable is set to 'Price'. The option to transform the target variable is enabled, and experiment logging is turned on.

#### Model Training: 
All available regression models are compared using PyCaret's compare_models function. The best-performing model is selected. Residuals and feature importance plots are generated using the plot_model function. The model is finalized and saved to disk.

#### Model Management with MLFlow: 
MLFlow's UI is started using !mlflow ui to manage experiments and models.

#### Consume the Model: 
The saved model is loaded using MLFlow, and predictions are made on a new dataset.

### Code Usage
Install necessary libraries:
#### pip install pycaret mlflow
#### Run the code in a Jupyter Notebook or Python environment.
#### Access the MLFlow UI by running !mlflow ui in the notebook and visiting localhost:5000 in your web browser.
#### Use the loaded model to make predictions on new data.

# 2: Model Registration and Versioning with MLFlow
### Description
This code demonstrates how to perform model registration and versioning using MLFlow. It trains an ElasticNet model for predicting wine quality, evaluates its performance, logs hyperparameters and evaluation metrics, and optionally registers the model in the MLFlow Model Registry for better management.

### Code Explanation
#### Setup and Data Loading: 
Necessary libraries are imported, and the wine quality dataset is read from a URL. The data is split into training and testing sets.

#### Model Training and Evaluation: 
An ElasticNet model is trained on the training data to predict wine quality. Performance metrics such as RMSE, MAE, and R2 are calculated for evaluation.

#### Ogging Parameters and Metrics: 
MLFlow is used to log the model's hyperparameters (alpha and l1_ratio) and evaluation metrics.

#### Model Registration (Optional): 
If not using a file store, the trained model is registered in the MLFlow Model Registry, enabling better versioning and management. If using a file store, the model is logged without registration.

### Code Usage
Install necessary libraries:
#### pip install pandas numpy scikit-learn mlflow
#### Run the code in a Python environment.
#### Check the MLFlow UI for experiment tracking and, if applicable, the registered model in the Model Registry.

Feel free to customize these explanations to better suit your documentation needs. Remember to include any installation instructions or prerequisites required to run the code successfully.



























