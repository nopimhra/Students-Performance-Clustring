# Student Performance Clustering Analysis  
*K-Means Clustering for Academic Behavior Segmentation*

## 📌 Project Overview
This project applies **unsupervised machine learning** to identify patterns in **student academic performance and engagement** using **K-Means Clustering**.  
The goal is to segment students into meaningful groups that can support **academic intervention, monitoring, and decision-making**.

Rather than predicting outcomes, this project focuses on **discovering hidden structures** in student behavior data.

---

## 🎯 Objectives
- Analyze student academic performance and attendance patterns
- Engineer meaningful behavioral features
- Apply K-Means clustering to segment students
- Interpret clusters in an academic decision-making context

---

## 📊 Dataset
- **Rows:** 300 students  
- **Features:** 16 original features  
- **Data type:** Tabular (academic scores & attendance)

### Key Feature Categories
- **Academic Performance:** quizzes, midterm, final exam, GPA
- **Engagement:** attendance, lab participation, assignment completion
- **Demographics:** age, gender

### Data Quality
- One feature contained missing values and was handled using **context-aware randomized imputation**
- No remaining missing values after preprocessing

---

## 🧠 Feature Engineering
Several composite features were created to better represent student behavior:

- **Quiz Average** – average quiz performance
- **Assignment Completion Rate** – task consistency indicator
- **Overall Attendance Rate** – engagement metric
- **Performance Index** – weighted academic score

These features help capture **both performance and behavioral consistency**.

---

## ⚙️ Data Preprocessing
- Feature scaling using **StandardScaler**
- Dimensionality reduction using **Principal Component Analysis (PCA)**

---

## 📉 Dimensionality Reduction (PCA)
- **Components used:** 2  
- **Explained Variance:** ~61%

### PCA Interpretation
- **PC1:** student engagement & discipline
- **PC2:** academic performance

PCA enables clear visualization of student segmentation in 2D space.

---

## 🔗 Clustering Method
- **Algorithm:** K-Means
- **Cluster selection:** Elbow Method
- **Optimal clusters:** **4**

Clustering was applied on standardized feature space and visualized in PCA space.

---

## 📈 Cluster Insights

| Cluster | Description |
|-------|-------------|
| Cluster 1 | High-performing, consistent, and highly engaged students |
| Cluster 2 | Academically capable but inconsistent engagement |
| Cluster 0 | Moderate performance with stable behavior |
| Cluster 3 | Low performance and low engagement (high-risk group) |

These clusters provide actionable insights for **academic support strategies**.

---

## 💡 Key Takeaways
- Student engagement is as important as academic scores
- Behavioral patterns can be identified without labeled outcomes
- Clustering enables early identification of at-risk students
- Results can support data-driven academic interventions

---

## 🛠 Tech Stack
- Python
- Pandas & NumPy
- Scikit-learn
- Matplotlib & Seaborn
- Google Colab
