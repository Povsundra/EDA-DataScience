
# Correspondence Analysis (CA)

## 📌 Overview
Correspondence Analysis (CA) is applied in this project to **explore and visualize the association between categorical variables**, with a focus on **household composition (number of children)** and **marital status**.  
CA complements the chi-square test by providing an **interpretable geometric representation** of how categories are related.

---

## 🎯 Objectives
- Test whether **Kids (number of children)** and **Marital Status** are statistically associated  
- Visually interpret **which categories are closely related**  
- Identify **dominant patterns** in household structure  
- Support insights used later in **customer segmentation (PCA + clustering)**

---

## 🧾 Variables Used

### Household Composition (Kids)
- No Kids  
- One Kid  
- Two Kids  
- Three or More Kids  

### Marital Status
- Single  
- Married  
- Together  
- Divorced  
- Widow  
- Rare categories (e.g., YOLO, Alone, Absurd – interpreted cautiously)

---

## 🔬 Methodology

1. **Data Preparation**
   - Created a `Kids` variable by summing `Kidhome` and `Teenhome`
   - Categorized `Kids` into meaningful household groups

2. **Chi-square Test of Independence**
   - Constructed a contingency table between `Kids_cat` and `Marital_Status`
   - Tested whether the two variables are independent

3. **Correspondence Analysis (CA)**
   - Applied CA only when the chi-square test was statistically significant
   - Performed Singular Value Decomposition (SVD) on standardized residuals
   - Retained the first two dimensions (Dim 1 and Dim 2)

4. **Visualization**
   - Generated a **symmetric CA biplot**
   - Interpreted distances, directions, and proximity of category points

---

## 📊 Key Results

- The first two CA dimensions explain **the majority of total inertia**, indicating a strong and reliable representation of the association.
- **Married** and **Together** categories are closely associated with households having **two or more children**.
- **Single** and **Widowed** individuals are primarily associated with **childless households** or those with one child.
- Rare marital status categories appear far from the origin, reflecting **distinct but low-frequency profiles**.

---

## 🧠 Interpretation Guidelines

- Categories **close together** → strong association  
- Categories **far from the origin** → high contribution to the association  
- Categories **opposite each other** → contrasting profiles  
- Rare categories should be interpreted with **caution** due to small sample sizes

---

## 🔗 Role in the Overall Project
Correspondence Analysis serves as an **exploratory bridge** between descriptive analysis and multivariate modeling:
- Confirms and explains categorical relationships identified by chi-square tests
- Provides behavioral and household insights used to interpret **PCA dimensions**
- Supports **customer profiling and segmentation** in later stages

---

## ✅ Summary
Correspondence Analysis reveals that **household composition and marital status are strongly associated**, with clear and interpretable family-structure patterns. These findings enrich the exploratory data analysis and strengthen the foundation for subsequent multivariate segmentation.

---
