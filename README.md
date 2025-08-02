# startup-success-prediction

<img src="notebooks/Startup_banner.avif" alt="Project Banner" style="width: 100%; height: auto;" />

Predicting startup success with Machine Learning on Crunchbase data for data-driven investment decisions.

---

## Table of Contents

- [Project Overview](#project-overview)  
- [Dataset Description](#dataset-description)  
- [Data Preprocessing](#data-preprocessing)  
- [Feature Engineering](#feature-engineering)  
- [Modeling](#modeling)  
- [Handling Class Imbalance](#handling-class-imbalance)  
- [Evaluation Metrics](#evaluation-metrics)  
- [Results](#results)  
- [How to Use](#how-to-use)  
- [Technologies Used](#technologies-used)  
- [Contributing](#contributing)  
- [License](#license)  
- [Contact](#contact)  

---

## Project Overview

This project develops Machine Learning models to predict whether startups are successful, fail, or remain operational using real-world Crunchbase data. The analysis leverages comprehensive feature engineering, advanced classification algorithms including Random Forest and Neural Networks, and addresses challenges like imbalanced classes through SMOTE. 

The aim is to support investors and stakeholders by providing actionable insights to drive data-driven decision making on startup investments.

---

## Dataset Description

The Crunchbase dataset used includes multiple features capturing startup funding rounds, employee growth, web presence, operating status, and other relevant business metrics. 

- **Source:** Crunchbase (public or licensed data)  
- **Key Features:** Funding rounds, funding value, employee count, web traffic, IPO status, acquisition status, and more.  
- **Target Variable:** Startup outcome classified as *Success*, *Failure*, or *Operational*.

---

## Data Preprocessing

- Handling missing values through imputation and default values.  
- Encoding categorical variables using label encoding and one-hot encoding where appropriate.  
- Scaling numerical features to normalize ranges and improve model convergence.  
- Parsing complex JSON-like fields to extract relevant information such as regions and funding details.

---

## Feature Engineering

Key engineered features include:

- Total funding amount and funding round count.  
- Employee growth metrics.  
- Web traffic statistics like monthly visits and growth rate.  
- Age of the company calculated from founding date.  
- Categorization of funding types and geographic regions.  

These features aim to capture critical indicators of startup health and growth potential.

---

## Modeling

- **Algorithms Used:** Random Forest Classifier and Neural Networks (TensorFlow).  
- Models trained to classify startups into three categories:  
  - **Success** (acquired, IPO, or Series B+ funding)  
  - **Failure** (closed or no Series B funding)  
  - **Operational** (active but not meeting success criteria)  

- **Training Techniques:**  
  - Hyperparameter tuning using RandomizedSearchCV for Random Forest.  
  - Early stopping and class weighting for Neural Networks.  

---

## Handling Class Imbalance

- SMOTE (Synthetic Minority Over-sampling Technique) applied to augment minority classes and balance the dataset for training.  
- Ensures fairer representation and improves prediction performance on less frequent classes.

---

## Evaluation Metrics

- Accuracy score for overall performance.  
- Confusion matrix to visualize class-wise prediction accuracy.  
- Classification report including precision, recall, and F1-score.  
- Feature importance analysis for Random Forest to understand key drivers of predictions.

---

## Results

- Random Forest achieved an accuracy of approximately 78%.  
- Neural Network achieved an accuracy of approximately 69%.  
- Feature importance highlights funding-related and growth features as primary indicators of startup success.  
- t-SNE visualization shows distinct clustering of success and failure groups in feature space.

---

## How to Use

1. Clone this repository:  
   ```bash
   git clone https://github.com/yourusername/startup-success-prediction.git

2. Navigate to the notebooks directory:
   ```bash
   cd startup-success-prediction/notebooks

3. Install required packages (see requirements.txt):
   ```bash
   pip install -r ../requirements.txt

4. Open and run the Jupyter Notebook:
   ```bash
   jupyter notebook Startup_Success_Prediction_Using_ML.ipynb

---

## Technologies Used

- Python 3.8+
- NumPy
- pandas
- scikit-learn
- TensorFlow
- imbalanced-learn (SMOTE)
- matplotlib
- seaborn
- Jupyter Notebook

---

## Contributing

Contributions are welcome! Feel free to:
- Submit issues for bugs or feature requests.
- Fork the repository and create pull requests with improvements.
- Suggest enhancements or new features.

Please ensure all contributions adhere to the existing code style and include appropriate documentation.

---

## License

This project is licensed under the MIT License.

---

## Contact

Divesh Chonkar  
Email: chonkar123divesh@gmail.com  
GitHub: https://github.com/DCodesIt

---

Thank you for checking out this project! 
