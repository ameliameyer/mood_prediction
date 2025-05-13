# Predicting Mood using Spotify Audio Features

Can machines detect the mood of a song?  This project uses Spotify audio features to classify songs as either 'happy' or 'not happy' based on their `valence` score.

---
## Motivation

Music plays a powerful role in shaping mood and emotion. By using audio features provided by Spotify, this project explores whether we can predict the emotional tone of a song — and what features are most influential in doing so.

---

## Dataset

The dataset includes audio features for thousands of songs, including:

- `danceability`
- `energy`
- `tempo`
- `acousticness`
- `valence` (used to derive the target label)

**Target Variable**:  
A binary label (`mood`) created from `valence`:
- `1` = happy (valence > 0.5)  
- `0` = not happy (valence ≤ 0.5)

## Modeling Approach

I trained and evaluated the following models:
- Logistic Regression
- Random Forest
- Support Vector Machine (SVM)
- XGBoost

Steps included:
- Data preprocessing and scaling
- Binary target transformation
- Model training and evaluation
- Comparison using accuracy and F1 score

## Results
| Model               | Accuracy | F1 Score |
|--------------------|----------|----------|
| Random Forest | 0.72| 0.72 |
| XGBoost | 0.71 | 0.71 |
| SVM | 0.71 | 0.71|
|Logistic Regression| 0.69| 0.69| 

The **Random Forest** performed best overall in terms of predictive power.

## Future Improvements

- Model valence as a regression or multi-class problem
- Include genre, lyrics, or user data
- Try deep learning on raw audio files or spectrograms

## Tools Used
- Python (Pandas, NumPy, Scikit-learn, Seaborn, Matplotlib)
- Kaggle/Jupyter Notebook
- Git & GitHub
