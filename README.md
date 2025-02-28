# MBTI Personality Classification with DeBERTa

![DeBERTa Logo](https://huggingface.co/microsoft/deberta-v3-base/resolve/main/logo.png)

## 🌟 Overview
This project classifies Myers-Briggs Type Indicator (MBTI) personality types based on social media posts using **DeBERTa-v3-base**, a transformer-based NLP model. The dataset consists of text samples labeled with one of the 16 MBTI personality types.

🚀 **Final Test Accuracy:** **49.11%**  
🔗 **Live Demo:** https://huggingface.co/spaces/aravindbethapudi2017/mbti

## 📂 Project Structure

## 🏆 Features
- **Deep Learning-based MBTI Classification** using `microsoft/deberta-v3-base`
- **Handles Imbalanced Classes** using stratified sampling & weighted loss
- **Deployed with Gradio** for an interactive web app
- **Available on Hugging Face Spaces & GitHub**

---

## 📊 Dataset
- **Source:** [Kaggle MBTI Dataset](https://www.kaggle.com/datasnaek/mbti-type)
- **Format:** CSV file with text posts & corresponding MBTI labels.
- **Classes:** 16 MBTI personality types (INFJ, ENTP, INTP, etc.)
  
### Sample:
| Text (Posts) | MBTI Type |
|--------------|----------|
| "I love deep discussions about philosophy." | INFJ |
| "Let's go out and have fun!" | ENFP |

---

## 🏗️ Model Training Pipeline
### 1️⃣ **Preprocessing**
- **Text Cleaning:** Removing URLs, special characters, and extra spaces.
- **Tokenization:** Using `AutoTokenizer` from Hugging Face.

### 2️⃣ **Training**
- **Model:** `microsoft/deberta-v3-base`
- **Optimizer:** AdamW (`lr=3e-5`)
- **Loss Function:** Weighted CrossEntropy to handle class imbalance
- **Stratified Sampling:** 80% Train / 20% Test split

### 3️⃣ **Evaluation**
- **Metrics:** Precision, Recall, F1-Score
- **Best Accuracy Achieved:** **49.11%**

---

## 🖥️ Deployment
This project is deployed using **Gradio** and **Hugging Face Spaces**.

### **Run Locally**
1. Clone the repository:
   ```bash
   git clone https://github.com/AravindBethapudi/MBTI-Classification.git
   cd MBTI-Classification
