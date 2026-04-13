# 🔐 LLM Phishing Bias, Fairness & Trustworthiness Analysis

**Author:** Savio Abraham  
**Program:** Master of Artificial Intelligence & Machine Learning  
**University:** University of Adelaide  

---

## 📌 Project Overview

This project evaluates **bias, fairness, and trustworthiness** in open-source Large Language Models (LLMs) within a **phishing vulnerability context**.

Using a prompt-based experimental pipeline, the study investigates:

- Whether LLMs show **systematic bias** in phishing vulnerability classification  
- Which **demographic attributes** influence predictions  
- How models behave in **trustworthiness scenarios** (e.g., phishing advice, adversarial prompts)  

The work is inspired by the **DECODINGTRUST framework**, focusing on:
- Fairness  
- Safety  
- Robustness  

---

## 🤖 Models Used

- `Qwen/Qwen2.5-7B-Instruct`  
- `Qwen/Qwen2.5-3B-Instruct`  
- `mistralai/Mistral-Nemo-Instruct-2407`  

---

## ⚙️ Methodology

### 🔹 Prompt-Based Pipeline

**Prompt 1 — Persona Generation**
- Generates 3 personas (A, B, C)
- Includes:
  - Age  
  - Gender  
  - Education  
  - Experience  
  - Profile details  

**Prompt 2 — Vulnerability Evaluation**
- Model selects the most vulnerable persona  
- Converted into:
  - 1 → Vulnerable (Yes)  
  - 2 → Non-Vulnerable (No)  

➡️ Each run = **3 samples**

---

## 📊 Dataset Summary

| Metric | Value |
|--------|------|
| Models | 3 |
| Prompt 2 Runs | 280 |
| Expected Samples | 900 |
| Final Samples | 840 |

Some samples were removed due to **invalid JSON outputs**.

---

## 📈 Statistical Analysis

The following tests were used:

- **Chi-square test** → Gender, Education, Region  
- **T-test** → Age, Experience  
- **Fisher’s Exact Test** → Selected relationships  

---

## 🛡️ Trustworthiness Evaluation

Models were evaluated on:

- ✅ Phishing victim support  
- ❌ Refusal of phishing generation (adversarial prompts)  
- 🔐 Privacy & security awareness  
- ⚖️ Ethical reasoning  
- ⚠️ Fairness & stereotype sensitivity  

---

## 🔍 Key Findings

### 📊 Bias & Patterns
- **Education** → Strongest predictor  
- **Experience** → Significant effect  
- **Age** → Small effect  
- **Gender** → No significant bias  
- **Region** → Unexpected pattern  

### 🤖 Trustworthiness
- ✔ Strong safety behaviour  
- ✔ Good refusal to malicious prompts  
- ⚠ Some fairness issues in sensitive scenarios  

---

## ⚠️ Limitations

- Synthetic dataset (not real-world data)  
- Imbalanced personas (gender, age)  
- Some invalid outputs removed  
- Manual trustworthiness evaluation  
- Limited number of models  

---

---

## 🚀 How to Run

1. Open notebook in **Google Colab**
2. Install dependencies:
   ```bash
   pip install transformers pandas numpy scipy matplotlib
   ```
