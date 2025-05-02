# 📩 SMS Spam Detection using Naive Bayes

This project implements a **Naive Bayes classifier** to detect spam messages in a dataset of SMS texts. It classifies each message as either **spam** or **ham** (not spam) using a simple and interpretable machine learning model.

## 📊 Dataset

The dataset used is `sms_spam.csv`, which contains SMS messages labeled as spam or ham.

### Sample Format:

| label | message                          |
|-------|----------------------------------|
| ham   | I'm gonna be home soon and i don't want to talk about this stuff anymore tonight... |
| spam  | Congratulations! You've won a $1000 Walmart gift card. Go to www.example.com to claim now. |

- `label`: Target column (spam or ham)
- `message`: SMS text content

## ⚙️ Features

- Text preprocessing: lowercase conversion, stopword removal, tokenization.
- Vectorization using TF-IDF.
- Naive Bayes classification (MultinomialNB).
- Accuracy evaluation and confusion matrix.

## 🛠️ Installation

```bash
git clone https://github.com/yourusername/sms-spam-naive-bayes.git
cd sms-spam-naive-bayes
pip install -r requirements.txt
```
🧠 Model :

We use the Multinomial Naive Bayes model, which works well for text classification problems where features are word frequencies or TF-IDF scores.


📈 Example Output

Accuracy: 0.985
Confusion Matrix:
[[965   0]
 [ 11 139]]
Classification Report:
              precision    recall  f1-score   support

         ham       0.99      1.00      1.00       965
        spam       1.00      0.93      0.96       150

    accuracy                           0.99      1115


📁 File Structure
```
sms-spam-naive-bayes/
│
├── sms_spam.csv                # Dataset
├── sms_spam_classifier.py      # Main Python script
├── README.md                   # Project documentation
├── requirements.txt            # Dependencies
```

📚 Dependencies :

pandas

scikit-learn

matplotlib (optional for plotting)

nltk

🧹 Future Improvements :

Hyperparameter tuning

Try other classifiers (e.g., SVM, Logistic Regression)

Deploy as a web app or API
