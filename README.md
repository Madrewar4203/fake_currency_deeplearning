# fake_currency_deeplearning
# 💵 AI-Counterfeit Currency Detection

This is a Flask-based deep learning web application that detects whether an uploaded **Indian currency note image** is **real or fake** using a trained **MobileNet** model. It also verifies if the uploaded image is relevant using a secondary PyTorch-based model before proceeding.

---

🚀 Features

- ✅ User Registration & Login System
- 📤 Upload currency note images (JPG, PNG, JPEG, JFIF)
- 🧠 Deep Learning model using MobileNet (TensorFlow/Keras)
- 🧪 Relevance Check using PyTorch MobileNetV2
- 💾 Stores prediction history for each user in MySQL
- 📊 View prediction history

---

🛠️ Tech Stack

| Layer        | Technologies                                 |
|--------------|----------------------------------------------|
| Frontend     | HTML, CSS (via Flask templates)              |
| Backend      | Python, Flask, MySQL                         |
| Deep Learning| TensorFlow (Keras), PyTorch, OpenCV, PIL     |
| Database     | MySQL                                        |

---

🧠 Model Info

🎯 Final Classification
- Model: `mobilenet.keras`
- Framework: TensorFlow/Keras
- Classes: `Real`, `Fake`

🔍 Relevance Checker
- Model: `mobilenet.pt`
- Framework: PyTorch
- Classes: `Relevant`, `Irrelevant`
- Ensures the uploaded image is an Indian currency note

---


2. Install Python Requirements
It’s recommended to use a virtual environment.

pip install -r requirements.txt
3. MySQL Setup
Create the database:

CREATE DATABASE fake_indian_currency;
Create the required tables:

CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    email VARCHAR(255),
    password VARCHAR(255)
);

CREATE TABLE history (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(255),
    path VARCHAR(255),
    results VARCHAR(50)
);


4. Run the Flask App

python app.py
Open http://127.0.0.1:5000 in your browser.
