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




