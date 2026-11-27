
# BookScope – Book Popularity Prediction

## About the Project

BookScope is a machine learning project where we explore what makes a book popular. We use the Goodreads Books dataset to understand how different book characteristics are related to popularity.

The main aim of this project is to classify books as popular or less popular using basic information such as author, genre, language, number of pages, title and description, without using ratings or reviews as model inputs.

## Dataset

We used the Goodreads Books dataset, which originally contained 20,068 records. After data cleaning, we had 19,941 records.

We divided books into two categories:

- **Popular:** Books with 10,000 or more ratings.
- **Less Popular:** Books with fewer than 10,000 ratings.

## Project Workflow

- **Data Cleaning:** Handled missing values and checked for duplicates and inconsistent data.
- **Exploratory Data Analysis (EDA):** Explored patterns and relationships between book characteristics and popularity.
- **Feature Engineering:** Created and selected relevant features for model training.
- **Model Training:** Used the CatBoost Classifier to classify books based on their popularity.
- **Model Optimisation:** Improved accuracy and precision by removing balanced class weights.
- **Evaluation and Visualisation:** Evaluated model performance and created visualisations to understand the results.

## Tools and Libraries Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- CatBoost
- Jupyter Notebook
- Google Colab

## Model Results

| Metric | Score |
|---|---:|
| Baseline Accuracy | 74.70% |
| Training Accuracy | 94.51% |
| Testing Accuracy | 88.23% |
| Precision | 79.19% |
| Recall | 72.54% |
| F1-Score | 75.72% |
| ROC-AUC | 0.9262 |
| Average Precision | 0.8291 |

The final CatBoost model achieved a testing accuracy of 88.23%, compared to the baseline accuracy of 74.70%.

## Key Findings

- Primary genre was the most important feature, followed by author and title length.
- Popular books generally had more pages and shorter titles than less-popular books.
- Books with known genre information were more likely to be popular.
- Removing class weights improved accuracy and precision but reduced recall.
- Missing book information may have influenced the model's predictions.

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
5. Run the notebooks in the following order:

   - Data_Cleaning.ipynb
   - EDA.ipynb
   - ML_Model_Training.ipynb
   - ML_Model_Training_Updated.ipynb
   - Visualisations.ipynb

## Conclusion

Through this project, we explored how machine learning can be used to understand and classify book popularity. Our results show that basic book information can be useful for popularity classification.

However, popularity was measured using Goodreads rating counts rather than actual book sales. Other factors such as marketing, reader preferences and missing book information may also influence the results.

## Future Work

- Predict the popularity of upcoming books before their publication.
- Include additional features such as publication dates, publisher information and marketing activity.
- Explore and compare other machine learning models.
- Test the model on newly published books to evaluate its reliability.


This project was completed as part of our academic coursework at Dublin City University.
