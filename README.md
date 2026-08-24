# 🔒 Phishing URL Detection

A machine learning web application that analyzes a URL and predicts whether it is **safe** or **phishing**. Built with Python, Flask, and a Gradient Boosting classifier trained on URL-based features.

## 🚀 Overview

Phishing websites trick users into revealing sensitive information by imitating legitimate sites. This project extracts 30 features from a given URL (such as use of IP addresses, URL length, presence of suspicious symbols, domain age, and more) and feeds them into a trained ML model to classify the URL and return a safety percentage.

## 🧠 How It Works

1. The user enters a URL in the web interface.
2. `feature.py` extracts 30 features from the URL (address-bar, domain, and HTML/JavaScript based features).
3. The pre-trained model (`model.pkl`) predicts whether the URL is safe or phishing, along with a confidence score.
4. The result is displayed to the user, with the option to proceed or stay safe.

## 🛠️ Tech Stack

- **Language:** Python
- **Web Framework:** Flask
- **Machine Learning:** scikit-learn (Gradient Boosting Classifier)
- **Feature Extraction:** BeautifulSoup, requests, python-whois, googlesearch
- **Frontend:** HTML, CSS
- **Deployment:** Gunicorn (Procfile included)

## 📂 Project Structure

```
phishing-url-detection/
├── app.py                 # Flask application
├── feature.py             # Extracts 30 features from a URL
├── requirements.txt       # Python dependencies
├── Procfile               # Deployment configuration
├── pickle/
│   └── model.pkl          # Trained ML model
├── templates/
│   └── index.html         # Web page
└── static/
    └── style.css          # Styling
```

## ⚙️ Run Locally

```bash
# Clone the repository
git clone https://github.com/kamalika1191-cloud/phishing-url-detection.git
cd phishing-url-detection

# Install dependencies
pip install -r requirements.txt

# Run the app
python app.py
```

Then open `http://127.0.0.1:5000/` in your browser.

## 📊 Features Extracted

The model uses 30 features grouped into categories:
- **Address bar based:** use of IP, long URLs, URL shortening, `@` symbol, redirects, prefix/suffix, sub-domains, HTTPS
- **Domain based:** domain registration length, DNS record, website traffic, domain age
- **HTML & JavaScript based:** iframe redirection, status bar customization, disabling right-click, website forwarding

## 📝 Note

This project is for educational purposes to demonstrate how machine learning can help detect phishing websites.
