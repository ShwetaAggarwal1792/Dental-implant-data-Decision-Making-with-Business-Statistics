# Implant Hardness Analysis by Dentist and Method

## 📖 Project Overview
This project analyzes how dental implant hardness varies based on:

- **Dentist**
- **Method used**
- **Interaction between Dentist and Method**

The analysis is performed separately for **Alloy Type 1** and **Alloy Type 2** using **Two-Way ANOVA** and post-hoc **Tukey HSD tests**.

**🎯 Objective**

- Determine whether implant hardness depends on the **Dentist**  
- Determine whether implant hardness depends on the **Method**  
- Determine whether there is a **Dentist × Method interaction effect**  

Understanding these relationships helps in process standardization and quality control in dental implant procedures.

---

## 📂 Dataset Description
The dataset contains:

| Column | Description |
|--------|-------------|
| Dentist | 5 dentists (Dentist 1 – Dentist 5) |
| Method | 3 implant preparation methods (Method 1 – Method 3) |
| Hardness | Measured hardness of dental implants |
| Alloy Type | Alloy Type 1 and Alloy Type 2 |

> Each Dentist–Method combination contains multiple observations.

---

## 🧪 Methodology

### 1️⃣ Exploratory Data Analysis (EDA)
- Verify data structure and data types
- Check for missing values
- Generate summary statistics
- Compute mean hardness by Dentist and Method

### 2️⃣ Hypothesis Testing
**Null Hypothesis (H₀):**  
There is **no interaction effect** between Dentist and Method on implant hardness.

**Alternate Hypothesis (Hₐ):**  
There is a **statistically significant interaction effect** between Dentist and Method on implant hardness.

### 3️⃣ Assumption Checks
- **Normality:** Shapiro-Wilk test on residuals  
- **Homogeneity of Variance:** Levene’s test  

> Two-Way ANOVA was used as it is robust to moderate assumption violations.

---

## 📊 Statistical Analysis

### 🔹 Alloy Type 1
- **Dentist effect:** Significant (p = 0.0115)  
- **Method effect:** Significant (p = 0.0003)  
- **Dentist × Method interaction:** Significant (p = 0.0068)  

> Indicates that the effect of the method depends on the dentist.

### 🔹 Alloy Type 2
- **Dentist effect:** Not significant (p = 0.3718)  
- **Method effect:** Significant (p < 0.001)  
- **Dentist × Method interaction:** Not significant (p = 0.0932)  

> Indicates that hardness is mainly influenced by the method, not by dentist-specific combinations.

---

## 🔍 Post-Hoc Analysis (Tukey HSD)
### Alloy Type 1
- Interaction effect is significant → Tukey HSD applied to all 15 Dentist–Method combinations  
- **Dentist 5 – Method 3** and **Dentist 4 – Method 3** showed the largest and most frequent significant differences  

### Alloy Type 2
- Post-hoc interaction analysis not performed  
- Differences are driven by the **Method factor** alone

---

## 📈 Key Insights
- Alloy Type 1 requires **dentist-specific optimization**  
- Alloy Type 2 supports **method standardization**  
- Interaction effects should not be ignored for Alloy Type 1

---


---

## 🛠️ Tools & Libraries Used
- **Python**  
- **pandas**  
- **numpy**  
- **scipy**  
- **statsmodels**  
- **matplotlib / seaborn**  
- **Jupyter Notebook**

---

## 🚀 How to Run
```bash
pip install pandas numpy scipy statsmodels matplotlib seaborn
