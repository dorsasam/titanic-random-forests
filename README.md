# Titanic Survival Prediction
This project involves using the Titanic dataset to predict whether a passenger survived the disaster. 
We fitted three models (Boosting, Bagging, and Random Forest) to determine the best tree-based model for this prediction task.

## Project Structure
- Part 1: Data Preparation
- Part 2: Model Training and Evaluation

## Dataset
The Titanic dataset contains information about passengers, including their survival status, demographics, and other relevant attributes. 
The dataset includes the following columns:
- **PassengerId**: Unique identifier for each passenger
- **Survived**: Survival status (0 = No, 1 = Yes)
- **Pclass**: Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd)
- **Name**: Name of the passenger
- **Sex**: Gender of the passenger
- **Age**: Age of the passenger
- **SibSp**: Number of siblings or spouses aboard the Titanic
- **Parch**: Number of parents or children aboard the Titanic
- **Ticket**: Ticket number
- **Fare**: Passenger fare
- **Cabin**: Cabin number
- **Embarked**: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)

##Project Steps
### Part 1: Data Preparation
- Loading the Dataset:
The dataset is loaded into a pandas DataFrame for analysis.
- Observing the Data:
Initial exploration of the data to understand its structure and identify any immediate issues.
- Removing Uninformative Columns:
Columns that do not provide useful information for predicting survival are removed.
- Encoding Categorical Features:
Categorical features are encoded using the one-hot encoding method to convert them into numerical values.
- Handling Missing Data:
Address missing values to ensure the dataset's completeness and accuracy.
- Extract the dependent and independent variable:
Identify the dependent variable (`Survived`), separating it from the rest of the DataFrame and keeping it as labels.
- Splitting the Dataset:
The dataset is split into training, development, and test sets to evaluate model performance at different stages.
### Part 2: Model Training and Evaluation
- Fitting Models:
Three models are fitted to the training data: Boosting, Bagging, and Random Forest.
The hyperparameters is set equal among the three models because we only intend to choose the best model at this stage. 
- Evaluating Models:
Each model's performance is evaluated on the development set to determine the best-performing model.
The metric used for this purpose is R2 Score.
- Selecting the Best Model:
Based on the evaluation metrics, the best tree-based model is selected.
- Tuning the Hyperparameters:
The hyperparameters of the best tree-based model are tuned based on the model's performance on the training and development sets with varying parameters.
- Final Evaluation:
The selected model's performance is evaluated on the test set to confirm its effectiveness.

## Installation
To run the project locally, follow these steps:
- Clone the repository:
```sh
git clone https://github.com/dorsasam/titanic-survival-prediction.git
cd titanic-survival-prediction
```
- Create a virtual environment and activate it:
```sh
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
```
- Install the required dependencies:
```sh
pip install -r requirements.txt
```
- Run the Jupyter notebooks or scripts as needed.
