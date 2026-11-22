# 🧬 ML Labs in Health, Biotech & Bioinformatics

I use this repository to collect my notes from machine-learning exercises relevant to health, biotechnology, and bioinformatics. The topics include regression, classification, and the safety of automated systems.

---

## 📁 Project Structure
```
ml-labs-health-bioinformatics/
├── data/                         # Raw and processed datasets
├── notebooks/                   # Jupyter notebooks with completed tasks
├── images/                      # Screenshots and plots from model outputs
├── reports/                     # Evaluation reports, classification reports
├── README.md                    # Project documentation
└── environment.yml              # Conda environment for reproducibility
```

---

## 🧪 Hands-on Lab 1: Investigating Insurance Charges (Regression)

**Objective:** Explore how age, BMI, smoking status, gender, and region affect health insurance pricing using a linear regression model via an interactive Streamlit app.

### 🔍 Tasks Overview
- **Task 1:** Highest Insurance Charge → A 60-year-old male smoker with high BMI.
- **Task 2:** BMI Distribution → Bell-curve shape; higher BMI linked to higher charges.
- **Task 3:** High-Risk Individual Simulation → Charge > $33,000 for 45yo male smoker.
- **Task 4:** Gender Distribution → Balanced dataset; no significant skew.
- **Task 5:** R² ≈ 0.75, RMSE ≈ 6000 (20% test split).
- **Task 6:** Smoker vs Non-Smoker → Huge jump ($33,000 vs ~$7,000).
- **Task 7:** Age 25 vs 65 → Prediction climbs from ~$4,000 to ~$13,000.
- **Task 8:** Regional Variance → Southeast had slightly higher charges.
- **Task 9:** Young Parent → Age 25 w/ 3 children → ~$6,000.
- **Task 10:** Gender Effects → Minimal when other variables are controlled.

---

## 🌸 Hands-on Lab 2: Iris Flower Classification (Multi-Class Classification)

**Objective:** Use a classification model to predict the species of iris flowers (Setosa, Versicolor, Virginica) based on petal/sepal dimensions.

### 📊 Key Metrics
**Initial Confusion Matrix (Low Accuracy):**
- Accuracy: 66.67%
- Versicolor misclassified as Virginica often.

**Optimized Confusion Matrix:**
- Accuracy: 96.67%
- Only 1 Virginica misclassified.

**Classification Report:**
```
              precision    recall  f1-score   support

      setosa       1.00      1.00      1.00        11
  versicolor       1.00      1.00      1.00        13
   virginica       1.00      1.00      1.00         6

    accuracy                           1.00        30
   macro avg       1.00      1.00      1.00        30
weighted avg       1.00      1.00      1.00        30
```

---

## 🧠 Theory Reading: Verifiably Safe Reinforcement Learning (VSRL)

**Objective:** Understand how safety is formally guaranteed in high-stakes ML environments (e.g., autonomous vehicles, drones).

### 🔑 Core Concepts
- **Safety Constraints:** Define limits (e.g., no collisions, obey rules).
- **Safe Exploration:** Train cautiously using simulations or conservative policies.
- **Verification:** Prove policies meet all safety guarantees mathematically.
- **Safe Policy Design:** Embed safety in reward design and action constraints.

### 🛠️ Practical Use Cases
- **Autonomous Driving**: Prevent red-light violations or collisions via verified policies.
- **Drone Delivery**: Avoid no-fly zones, maintain altitude and safety through formal verification and constraint learning.

---

## 🧬 Relevance to Bioinformatics & Biotech
- **Regression modeling** parallels risk scoring or predicting gene expression.
- **Classification** mirrors tasks like disease classification or phenotype labeling.
- **Safe RL principles** can be adapted for lab automation, clinical robotics, or genetic testing pipelines.

---

## Interpretation and limitations
- **Bias Audits:** Smoker and age effects dominate prediction—caution needed.
- **Gender & Regional fairness:** Model behaved consistently; but continuous monitoring is critical.
- **Transparency:** Feature selection and output plots ensure interpretability.

---

## 🚀 Getting Started
1. **Clone the repo**
```bash
git clone https://github.com/mkromah/ML4Biotech-HandsOnLabs.git
```
2. **Setup environment**
```bash
cd ML4Biotech-HandsOnLabs
conda env create -f environment.yml
conda activate insurance-ml
```
3. **Run notebooks or launch the Streamlit App**

---

## 🙌 Credits
- **Lab Author:** Lakshmi Holla
- **Contributor:** Malika Singla


---

## 🤝 Contributions Welcome
I welcome corrections and suggestions for additional exercises in genomics, laboratory applications, or model evaluation.
