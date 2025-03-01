# 📰 Fake News Detection using Machine Learning  

## 📌 Overview  
This project aims to classify news articles as **FAKE** or **REAL** using the **Linear SVC** model.  
It uses **TF-IDF Vectorization** for text processing and achieves an accuracy of **94.39%**.  

📌 **Dataset Used:** [fake_or_real_news.csv](https://github.com/lutzhamel/fake-news/blob/master/data/fake_or_real_news.csv)  

---

## 📊 Dataset Information  
The dataset contains **6,335** news articles with the following columns:  

| Column | Description |
|--------|------------|
| `id` | Unique identifier |
| `title` | Headline of the article |
| `text` | Full news content |
| `label` | `FAKE` (Fake News) or `REAL` (Genuine News) |

🔹 Labels are converted into **numerical values**:  
- `REAL` → **0**  
- `FAKE` → **1**  

---

## 🚀 How It Works  
🔹 **Step 1:** Load and preprocess the dataset  
🔹 **Step 2:** Split the data into **training (80%)** and **testing (20%)**  
🔹 **Step 3:** Convert text into numerical data using **TF-IDF Vectorizer**  
🔹 **Step 4:** Train the **Linear SVC model**, one of the best for text classification  
🔹 **Step 5:** Evaluate model accuracy (**94.39%**)  
🔹 **Step 6:** Predict whether new articles are **FAKE** or **REAL**  


## 🔥 Why LinearSVC?  
✅ **Fast & Efficient** – Works well for large text datasets  
✅ **Handles High-Dimensional Data** – Effective for text classification  
✅ **High Accuracy** – Achieves **94.39%** on this dataset  

---

## 📝 How to Test Your Own News Articles?  
You can add your own news articles and check if they are **FAKE** or **REAL**!  

### **Steps to Add Custom News Articles**  
1️⃣ **Create a text file** (e.g., `my_news.txt`) and write a news article inside.  
2️⃣ **Modify the code** to read this file and process it.  
3️⃣ **Run the code** to get the prediction.  

### **Code to Check Custom News Articles**  

# Load your custom news article
with open("my_news.txt", "r") as file:
    article_text = file.read()

# Vectorize and predict
vectorized_text = vectorizer.transform([article_text])
prediction = clf.predict(vectorized_text)

# Display result
print("FAKE NEWS" if prediction[0] == 1 else "REAL NEWS")

