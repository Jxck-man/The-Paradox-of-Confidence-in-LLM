# The-Paradox-of-Confidence-in-LLM

## 📜 Abstract
Large Language Models (LLMs) like OpenAI’s GPT series and Anthropic’s Claude have demonstrated remarkable capabilities in generating fluent, context-aware responses. However, this research investigates a critical question: **Do LLMs exhibit higher verbal confidence when they are wrong?**  
Using the **TruthfulQA** and **MMLU** datasets, we analyze how verbal confidence correlates with factual correctness, exploring differences across models and difficulty levels.

---

## 📊 Dataset Details
### 1. TruthfulQA  
- Focuses on factuality and truthfulness.
- Contains challenging, ambiguous, and knowledge-based questions.
- Categories: Misconceptions, Superstitions, and more.

### 2. MMLU (Massive Multitask Language Understanding)  
- Covers 57 subject areas.
- Divided into **easy** and **hard** questions based on complexity.
- Measures both reasoning and domain-specific knowledge.

**Data Source:**  
- [TruthfulQA on Hugging Face](https://huggingface.co/datasets/domenicrosati/TruthfulQA)  
- [MMLU on Hugging Face](https://huggingface.co/datasets/cais/mmlu)  

---

## ⚙ Methodology
1. **Model Selection**
   - OpenAI GPT-3.5
   - Claude 3.5 Sonnet
   - Claude 3 Haiku

2. **Confidence Scoring Framework**
   - Linguistic confidence cues (assertiveness, lack of hedging)
   - Numerical ratings when provided by the model
   - Custom parsing to measure certainty levels

3. **Evaluation Procedure**
   - Ask each question from both datasets
   - Record model responses and self-reported confidence (if available)
   - Classify responses as **Correct** or **Incorrect**
   - Compare average confidence levels in both cases

4. **Analysis Dimensions**
   - Model-wise comparison
   - Dataset-level trends
   - Easy vs. Hard question performance

---

## 📈 Results & Findings
- **Key Observation:** Certain models display **higher verbal confidence** in incorrect answers than correct ones.
- **Easy vs. Hard:** Confidence bias was more pronounced in **hard** questions for all models.
- **Model Trends:**  
  - GPT-3.5 showed moderate bias but higher consistency.
  - Claude Sonnet had the largest confidence gap between wrong and right answers.
  - Claude Haiku was less assertive overall.

> 📌 **Full detailed results with visualizations are included in the `/results` folder.**

---

## 📌 How to Run the Code
### **1. Clone the Repository**
```bash
git clone https://github.com/YOUR-USERNAME/The-Paradox-of-Confidence-in-LLM.git
cd The-Paradox-of-Confidence-in-LLM

