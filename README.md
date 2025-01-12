# Machine Learning Course Project (CS 412)

Welcome to the repository for the CS 412 Machine Learning course project. This repository contains all files, notebooks, scripts, and results required for completing the project tasks, including regression and classification for multiple rounds.

---




# Project Overview

This project involves building regression and classification models to analyze social media accounts. It is divided into the following stages:

1. **Data Annotation**  
   Annotating profile metadata and posts for training data.

2. **Feature Extraction and Modeling**  
   Developing machine learning models to classify account types and predict post engagement.

3. **Competition**  
   Submitting predictions in three rounds for evaluation.

## Instructions

### 1. Clone the Repository
Clone this repository to your local machine using the following command:

git clone https://github.com/your-username/ML_Project_CS412.git
cd ML_Project_CS412


### 2. Install Dependencies
Install the required Python libraries by running the following command:

pip install -r requirements.txt

### 3. Data Files
- **Raw Data**: Training and test files are located in the `data/raw_data/` directory.
- **Annotated Data**: Annotated data for four users is located in the `data/annotated_data/` directory.

### 4. Notebooks
The following Jupyter notebooks are included for various tasks:
- **`round1_regression_classification.ipynb`**: Implements both regression and classification for Round 1.
- **`regression_round2.ipynb`**: Implements regression for Round 2.
- **`classification_round2.ipynb`**: Implements classification for Round 2.
- **`annotation_analysis.ipynb`**: Analyzes the annotated data.

#### Run the notebooks with Jupyter:
To run the notebooks, execute the following command in the terminal:
jupyter notebook

## Methodology

## Progression Through Rounds

### Round 1

In Round 1, we focused on applying basic machine learning techniques without heavily preprocessing the data or addressing class imbalance. The dataset was kept mostly as-is, and we passed the data directly through the machine learning model. This approach yielded reasonable results but revealed the limitations of unbalanced datasets.

#### Classification Results:

**Accuracy:** 0.80531 (Rank 80/141)

**F1-weighted:** 0.694727 (Rank 64/141)

#### Regression Results:

**Error:** 4901.286817 (Rank 103/141)

### Round 2

For Round 2, we aimed to improve classification performance by balancing the dataset. We dropped classes with very few values based on the hypothesis that a balanced dataset would enhance model accuracy. Despite balancing the data, the inherent imbalance in the test data negatively impacted the model's generalization, resulting in a significant decrease in classification accuracy.

#### Classification Results:

**Accuracy:** 0.81057 (Rank 109/138)

**F1-weighted:** 0.354373 (Rank 109/138)

#### Regression Results:

**Error:** 1429.240571 (Rank 63/138)

This round highlighted the importance of carefully handling class imbalance while considering the nature of the test data.

### Round 3

In Round 3, we revisited our approach by reusing the code from Round 2 but with additional fine-tuning and adjustments based on insights gained from previous rounds. The final models aimed to better generalize on imbalanced test data while maintaining a balanced approach during training.

### Data Preprocessing

#### Classification Task:

**Data Loading:** Profile metadata and posts data were loaded.

Handling Missing Data: Missing values were imputed using median values for numerical fields and mode for categorical fields.

**Feature Engineering:**

Extracted relevant features from metadata, such as the number of posts, average post engagement, and account bio keywords.

Text data from posts were vectorized using TF-IDF.

**Normalization:** Numerical features were normalized using Min-Max scaling to improve model performance.

#### Regression Task:

**Data Loading:** Post-level data was loaded and cleaned.

**Log Transformation:** The like count was log-transformed to handle heavy-tailed distributions and improve model stability.

**Feature Selection:**

Extracted features such as post length, hashtag count, and media type (image, video).

Engineered interaction features between engagement metrics and account popularity.

**Splitting Data:** Data was split into training and test sets with an 80-20 ratio.

### Model Training

#### Classification Task:

**Model Selection:** Various models were tested, including Logistic Regression, Random Forest, and XGBoost.

**Hyperparameter Tuning:** Grid search was used to find the optimal hyperparameters for each model.

**Final Model:** XGBoost was selected based on its superior accuracy and robustness to imbalanced classes.

#### Regression Task:

**Model Selection:** Linear Regression, Ridge Regression, and Gradient Boosting Regressor were evaluated.

**Hyperparameter Tuning:** Cross-validation was applied to determine the best regularization parameters.

**Final Model:** Ridge Regression was chosen due to its lower mean squared error (MSE) on the validation set.

### 5. Results
- **Predictions for Each Round**:
  - **Round 1**: Predictions and rankings are saved in the `results/round1/` directory.
  - **Round 2**: Predictions and rankings are saved in the `results/round2/` directory.
  - **Round 3**: Predictions are saved in the `results/round3/` directory.

- **Submitted Files**:
  - **Classification**:
    - `prediction-classification-round1.json`
    - `prediction-classification-round2.json`
    - `prediction-classification-round3.json`
  - **Regression**:
    - `prediction-regression-round1.json`
    - `prediction-regression-round2.json`
    - `prediction-regression-round3.json`

---

### Annotated Data
The `data/annotated_data/` directory contains manually annotated data for four users. Each file is in JSON format with the following structure:

{
    "user_id": "12345",
    "annotations": [
        {
            "post_id": "post1",
            "category": "fitness",
            "like_prediction": 150
        }
    ]
}

### Team Members
- **Hamza Wasim**
- **Azman Morani**
- **Muhammad Abdul Salam**
- **Ramiz Khan Niazi**
- **Amin Zaka**

---

### Analysis of Findings

#### **Classification Results**:
- **Round 1**:
  Classification accuracy: 0.80531 (Rank 80.0/141) --- Classification f1-weighted: 0.694727 (Rank 64.0/141)

- **Round 2**:
  - Classification accuracy: 0.81057 (Rank 109.0/138) --- Classification f1-weighted: 0.354373 (Rank 109.0/138)

- **Round 3**:
  - Final accuracy: **%**. The inclusion of more balanced training data significantly improved overall results.

---

#### **Regression Results**:
- **Round 1**:
  - Regression error: 4901.286817 (Rank 103.0/141)

- **Round 2**:
  - Regression error: 4084.867489 (Rank 111.0/138)


---

### License
This project is licensed under the **MIT License**. See the `LICENSE` file for details.




