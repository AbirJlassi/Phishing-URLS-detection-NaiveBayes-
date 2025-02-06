# **Phishing URL Detection using Naïve Bayes**

## **Project Overview**
This project focuses on detecting phishing URLs using the Naïve Bayes classification algorithm. The goal is to build a machine learning model that can distinguish between legitimate and phishing websites based on extracted features from URLs.

## **Dataset**
- The dataset contains **651,191 URLs** classified into four categories:
  - **Benign (Legitimate):** 428,103 URLs
  - **Defacement:** 96,457 URLs
  - **Phishing:** 94,111 URLs
  - **Malware:** 32,520 URLs
- The dataset is labeled, allowing supervised learning techniques to be applied.

## **Some of the Features Used for Classification**
The following features are extracted from each URL:
- **URL Length** – Phishing URLs tend to be longer.
- **Number of Dots (.)** – More dots often indicate subdomains used in phishing.
- **Number of Subdomains** – Suspicious subdomains can be an indicator.
- **Presence of Suspicious Characters (@, -, _, etc.)** – Phishing URLs often use misleading characters.
- **Use of Shortened URLs** – Bit.ly, TinyURL, etc., are commonly used in phishing.
- **Entropy of URL** – Higher entropy means more randomness, which may indicate phishing.
- **Top-Level Domain (TLD) Analysis** – Certain TLDs are frequently associated with phishing.
- **Presence of Sensitive Words** – Words like "secure", "login", or "bank" are analyzed.

## **Model Implementation**
- The **Gaussian Naïve Bayes** classifier is used since it handles continuous variables efficiently.
- **Scikit-learn** is utilized for model training, evaluation, and testing.
- **Train-Test Split:** 80% training, 20% testing.

## **Steps for Implementation**
1. **Data Preprocessing:**
   - Import dataset and clean data.
   - Extract URL-based features.
   - Encode categorical values.
2. **Feature Engineering:**
   - Apply transformation techniques to extract meaningful insights.
3. **Model Training:**
   - Train Gaussian Naïve Bayes on extracted features.
4. **Evaluation:**
   - Compute accuracy, precision, recall, and F1-score.
   - Generate confusion matrix for performance insights.
5. **Testing on New URLs:**
   - Simulate real-world cases with unseen URLs.

## **Results**
- **Accuracy:** 89.5%
- **Precision (Legitimate):** 90.7%, **Recall:** 94.7%
- **Precision (Phishing):** 83.1%, **Recall:** 73.0%
- **Observations:**
  - The model effectively detects **legitimate URLs**.
  - Detection of **phishing URLs** can be improved with better feature engineering.


## **Dependencies**
Install the required Python libraries:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn
