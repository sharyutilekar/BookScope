# BookScope – Book Popularity Prediction

## About the Project

BookScope is a machine learning project where we explore what makes a book popular. We use the Goodreads Books dataset to understand how different book characteristics are related to popularity.

The main aim of this project is to predict whether a book is likely to become popular using basic information such as its author, genre, language, number of pages, title and description, without using existing ratings or reviews.

## Dataset

We used the Goodreads Books dataset, which originally contained 20,068 records. After data cleaning, we had 19,941 records.

We divided books into two categories:

- **Popular:** Books with 10,000 or more ratings.
- **Less Popular:** Books with fewer than 10,000 ratings.

## Project Workflow

- **Data Cleaning:** Cleaned the dataset by handling missing values and checking for duplicates and inconsistent data.
- **Exploratory Data Analysis (EDA):** Explored the dataset to understand different patterns and relationships between book characteristics and popularity.
- **Feature Engineering:** Selected and created relevant features for model training.
- **Model Training:** Used the CatBoost Classifier to predict book popularity.
- **Evaluation and Visualisation:** Evaluated the model and created visualisations to better understand the results.

## Tools and Libraries Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- CatBoost
- Jupyter Notebook and Google Colab

## Model Results

| Metric | Score |
|---|---:|
| Baseline Accuracy | 74.70% |
| Model Accuracy | 88.23% |
| Precision | 79.19% |
| Recall | 72.54% |
| F1-Score | 75.72% |
| ROC-AUC | 0.9262 |

Our updated CatBoost model achieved an accuracy of 88.23%, which is higher than the baseline accuracy of 74.70%.

## Project Structure

```text
BookScope/
├── Data/
│   ├── Goodreads Books.csv
│   ├── Goodreads Books Cleaned.csv
│   └── Goodreads Books EDA.csv
├── Notebook/
│   ├── Data_Cleaning.ipynb
│   ├── EDA.ipynb
│   ├── ML_Model_Training.ipynb
│   ├── ML_Model_Training_Updated.ipynb
│   └── Visualisations.ipynb
└── README.md
```

## How to Run the Project

1. Download or clone this repository.
2. Install the required Python libraries.

```bash
pip install pandas numpy matplotlib seaborn scikit-learn catboost notebook
```

3. Open the notebooks in Jupyter Notebook or Google Colab.
4. Update the dataset paths if needed.
5. Run the notebooks in order, starting with data cleaning, followed by EDA, model training and visualisation.

## Conclusion

Through this project, we learned how machine learning can be used to predict book popularity using basic book information. Our results show that book characteristics can help estimate popularity without using existing ratings or reviews. However, other factors such as marketing and social media trends may also influence a book's popularity.
