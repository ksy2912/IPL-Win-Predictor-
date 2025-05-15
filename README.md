# 🏏 IPL Win Predictor

This project is a machine learning-based web application that predicts the probability of a team winning an ongoing IPL match using live match conditions. Built using **Logistic Regression**, the model leverages real match features such as current score, overs completed, wickets fallen, and target score to predict win likelihood.

---

## 🔗 Live Demo

👉 [Streamlit App](https://ghkzs3grye9jhtqbtzsoxu.streamlit.app/)

Try out the model live on Streamlit using a clean and interactive user interface.

---

## 🖼️ App UI Screenshot

Below is a preview of the deployed web application:

![image](https://github.com/user-attachments/assets/a06e86c2-496e-44a2-8ade-3157ac2b9256)


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


## 🎯 Model Architecture

### ✅ Model: Logistic Regression
A simple yet effective binary classification model that estimates the probability of a team **winning or losing** based on current match stats.

### 📊 Dataset
- Compiled from IPL datasets containing ball-by-ball and match-level data.
- Historical match data from 2008 to 2020 used for training.

### 🔢 Features

Derived and selected key features:

| Feature               | Description                                      |
|----------------------|--------------------------------------------------|
| Batting team         | Team currently batting                          |
| Bowling team         | Opponent bowling team                           |
| Host city            | City where the match is played                  |
| Target               | Total score to win                              |
| Current score        | Current score of the batting team               |
| Overs completed      | Overs completed in second innings               |
| Wickets out          | Number of wickets lost                          |
| Balls remaining      | 120 - (overs completed * 6)                     |
| Runs required        | Target - Current score                          |
| Wickets in hand      | 10 - Wickets out                                |
| Current run rate     | Current score / overs completed                |
| Required run rate    | Runs required / (balls remaining / 6)          |

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
## 📈 Model Performance

The model was evaluated using standard classification metrics:

- Accuracy: ~80% (on validation set)
- ROC AUC Score: ~0.85
- Precision & Recall metrics were balanced  

---

## 🧠 Features Engineering & Preprocessing

- Encoded categorical variables (Teams, City) using OneHotEncoder
- Removed features not available mid-match (like match winner)
- Engineered additional context-based features (e.g., run rate, wickets remaining)
- Split into training and test sets with stratified sampling
- Scaled numerical features

---

## 🗂️ Repository Structure
IPL-Win-Predictor-/
├── app.py                   # Streamlit web app
├── ipl_win_predictor.ipynb  # EDA and model training notebook
├── model.pkl                # Trained logistic regression model
├── requirements.txt         # Project dependencies
├── ipl_app_ui_screenshot.png  # Screenshot image for README
└── README.md                # Project documentation

---
## 📚 How to Run Locally

### 👉 Requirements
- Python 3.7+
- pip or conda

---

### 🔧 Setup Steps

```bash
git clone https://github.com/ksy2912/IPL-Win-Predictor-.git
cd IPL-Win-Predictor-
pip install -r requirements.txt
```

---

### ▶️ Launch the App

```bash
streamlit run app.py
```

---

### 🛠️ Future Improvements

- Incorporate more granular features (e.g., bowler stats, recent performance)
- Use more advanced models (e.g., XGBoost, Random Forest)
- Integrate with live match APIs for real-time predictions
- Add charts for win probability trends over time

---
## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch: `git checkout -b feature/YourFeature`.
3. Commit your changes: `git commit -m 'Add your feature'`.
4. Push to the branch: `git push origin feature/YourFeature`.
5. Open a pull request.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 📬 Contact

For any inquiries or feedback, please contact [your email address].

---
