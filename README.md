# 🚗 Car Price Predictor
 
A complete end-to-end Machine Learning web application that predicts the selling price of used cars based on their specifications. 

**🔴 Live App:** [https://car-price-predictor-1-8u8k.onrender.com](https://car-price-predictor-1-8u8k.onrender.com)<br>
*(Note: Since this is hosted on a free tier, it may take 30-50 seconds to wake up the server on the first load).*

---

## 📖 Project Overview
This project takes historical data of used cars and applies a Linear Regression model to estimate the current market value of a vehicle. It includes a complete data pipeline, from cleaning messy real-world data to training a predictive model, and features a user-friendly web interface where users can input car details to get an instant price estimation.

## ✨ Features
*   **Accurate Predictions:** Utilizes a trained machine learning model that achieved an R² score of ~0.899 on the test dataset.
*   **Dynamic Web Interface:** Features a responsive frontend using Bootstrap 4 that dynamically filters available car models based on the selected manufacturing company.
*   **Instant Results:** Processes user input via a backend API using AJAX to generate real-time price predictions without reloading the page.

## 🛠️ Tech Stack
*   **Machine Learning & Data Processing:** Python, Pandas, NumPy, Scikit-Learn (v1.4.2)
*   **Web Framework (Backend):** Flask and Flask-CORS for handling API requests and serving the model
*   **Frontend UI:** HTML, CSS, Vanilla JavaScript, and Bootstrap 4
*   **Deployment:** Render.com with Gunicorn WSGI server

---

## 🧠 Model & Data Details
*   **Data Preprocessing:** The raw dataset contained irregularities such as non-numeric years, text mixed with integer values (e.g., "kms", "Ask For Price"), and missing fields. The data was thoroughly cleaned, and car names were standardized to their first three words for better categorical grouping. The cleaned data was saved as `Cleaned_Car.csv`.
*   **Model Architecture:** The core algorithm is a Multiple Linear Regression model.
*   **Pipeline Integration:** To seamlessly handle raw text inputs from the user, the model is packaged inside a Scikit-Learn `Pipeline` alongside a `ColumnTransformer` and `OneHotEncoder`. This ensures that categorical variables (Name, Company, Fuel Type) are automatically converted into binary matrices before making predictions.

---

## 🚀 How to Run Locally

### 1. Clone the repository
```bash
git clone https://github.com/vaidya21/Car-Price-Predictor.git
cd Car-Price-Predictor
```
