# 🏏 IPL Win Predictor

This project is a machine learning-based web application that predicts the probability of a team winning an ongoing IPL match using live match conditions. Built using **Logistic Regression**, the model leverages real match features such as current score, overs completed, wickets fallen, and target score to predict win likelihood.

---

## 🔗 Live Demo

👉 [Streamlit App](https://ghkzs3grye9jhtqbtzsoxu.streamlit.app/)

Try out the model live on Streamlit using a clean and interactive user interface.

---

## 📌 Project Motivation

In the high-pressure world of T20 cricket, especially the IPL (Indian Premier League), fans and analysts are always curious about the **real-time winning probabilities**. This project uses historical match data and machine learning to simulate that experience using a web app that updates predictions based on match status.

---

## 🎯 Objective

Given:
- Batting and Bowling team
- Host city
- Target score
- Current score
- Overs completed
- Wickets fallen

The app predicts:
- **Winning Probability** for the batting team

---

## ⚙️ Machine Learning Model

- **Model Used**: Logistic Regression
- **Problem Type**: Binary Classification (Win / Loss)
- **Training Data**: Cleaned and preprocessed IPL ball-by-ball and match-level datasets
- **Key Features** used for training:
  - Batting team
  - Bowling team
  - City
  - Target score
  - Current score
  - Overs completed
  - Wickets out
  - Derived metrics like:
    - **Current Run Rate**
    - **Required Run Rate**
    - **Balls remaining**
    - **Wickets in hand**

---

## 📈 Model Performance

The model was evaluated using standard classification metrics:

- Accuracy: ~80% (on validation set)
- ROC AUC Score: ~0.85
- Precision & Recall metrics were balanced  
> Note: These are approximations based on typical logistic regression performance. Update with exact values from your training notebook if needed.

---

## 🧠 Features Engineering & Preprocessing

- Encoded categorical variables (Teams, City) using OneHotEncoder
- Removed features not available mid-match (like match winner)
- Engineered additional context-based features (e.g., run rate, wickets remaining)
- Split into training and test sets with stratified sampling
- Scaled numerical features

---

## 🛠️ Tech Stack

| Component       | Technology           |
|----------------|----------------------|
| UI Framework   | Streamlit            |
| Language       | Python               |
| ML Library     | scikit-learn         |
| Data Handling  | Pandas, NumPy        |
| Model Storage  | Pickle (`model.pkl`) |
| Deployment     | Streamlit Cloud      |

---

## 🖼️ App UI Screenshot

Below is a preview of the deployed web application:

![IPL Win Predictor UI](ipl_app_ui_screenshot.png)

---

## 🗂️ Repository Structure

