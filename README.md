# 🛡️ Phishing Email Detector — Chrome Extension

A machine learning-powered Chrome extension that detects phishing emails in real-time. Built as part of coursework at **San José State University** (CMPE 255 — Data Mining).

## 🎯 Overview

Phishing attacks remain one of the most common cybersecurity threats. This extension analyzes email content directly in the browser using a pre-trained ML model to classify emails as **safe** or **phishing** — giving users instant visual feedback.

## ✨ Features

- **Real-Time Detection** — Scans email content on the active page
- **ML-Powered** — Uses a scikit-learn model trained on 18,000+ labeled phishing/legitimate emails
- **Chrome Extension** — Manifest V3, lightweight popup UI
- **Pre-trained Model** — Serialized `phishing_model.pkl` and `vectorizer.pkl` ready to use
- **Visual Alerts** — Clear popup interface showing phishing probability

## 🏗️ Architecture

```
PhishingDetectorExtension/
├── manifest.json          # Chrome Extension config (Manifest V3)
├── popup.html             # Extension popup UI
├── popup.js               # Popup logic & API calls
├── background.js          # Service worker for background tasks
├── main.js                # Content script injected into web pages
├── model/
│   ├── phishing_model.pkl # Trained ML classification model
│   └── vectorizer.pkl     # TF-IDF text vectorizer
├── src/
│   └── Main.java          # Model training pipeline
└── Phishing_Email.csv     # Dataset (18,000+ samples)
```

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Extension** | Chrome Manifest V3, JavaScript, HTML/CSS |
| **ML Model** | Python, scikit-learn, TF-IDF Vectorization |
| **Training** | Java (data preprocessing), Jupyter Notebook |
| **Dataset** | 18,000+ labeled phishing/legitimate emails (CSV) |

## 🚀 Getting Started

### Load the Extension in Chrome

1. Clone this repo:
   ```bash
   git clone https://github.com/amanimran786/PhishingDetectorExtension.git
   ```
2. Open Chrome → `chrome://extensions/`
3. Enable **Developer Mode** (toggle in top-right)
4. Click **"Load unpacked"**
5. Select the `PhishingDetectorExtension` folder
6. The extension icon will appear in your toolbar

### Usage

1. Navigate to a page with email content
2. Click the extension icon in the Chrome toolbar
3. The popup displays the phishing risk assessment

## 📊 Model Details

- **Algorithm:** scikit-learn classifier with TF-IDF feature extraction
- **Dataset:** `Phishing_Email.csv` — 18,000+ labeled samples
- **Features:** Text content vectorized using TF-IDF
- **Output:** Binary classification (Phishing / Legitimate) with confidence score

## 👨‍💻 Author

**Aman Imran** — B.S. Software Engineering, San José State University
- 📧 [aman.imran@sjsu.edu](mailto:aman.imran@sjsu.edu)
- 🔗 [LinkedIn](https://www.linkedin.com/in/aman-i-636013111/)
- 🌐 [Portfolio](https://aman-portfolio-green.vercel.app/)

## 📄 License

This project is open source and available for educational purposes.
