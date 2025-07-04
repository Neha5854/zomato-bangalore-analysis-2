
# 🍽 Zomato Restaurant Delivery Prediction (Capstone Project)

This project builds a machine learning model to predict whether a restaurant offers home delivery, based on real-world Zomato Bangalore data. The goal is to explore business patterns and create a predictive system using classification models.

---

##  Objective

To predict the `IsHomeDelivery` status of a restaurant using features like location, cuisine variety, and takeaway availability. The model helps businesses understand delivery behavior and make better operational decisions.

---

##  Dataset

- **Source:** Zomato Bangalore Restaurants dataset (CSV format)
- **Size:** ~9500+ restaurant records
- **Target Variable:** `IsHomeDelivery` (0 = No, 1 = Yes)

---

##  Data Preprocessing

- Null value handling
- Feature engineering:
  - `CuisineCount` (number of cuisines offered)
  - One-hot encoding for categorical variables
- Removed duplicates and outliers

---

##  Exploratory Data Analysis (EDA)

- Distribution of delivery vs non-delivery restaurants
- Top cuisines, areas, and restaurant types
- Correlation heatmaps and feature relationships
- Feature importance visualization (Random Forest)

---

##  Models Used

| Model               | Accuracy | Notes |
|--------------------|----------|-------|
| Logistic Regression | 70.2%    | Captured minority class better (fairer) |
| Random Forest       | 97.6%    | High overall accuracy but biased toward majority class |

### ⚖ Handling Class Imbalance

- Applied `class_weight='balanced'` in both models
- Explained trade-off: **accuracy vs fairness**
- Discussed limitations and potential improvements (e.g., SMOTE)

---

##  Results

- Random Forest with `class_weight='balanced'` achieved **97.6% accuracy**
- Logistic Regression achieved **70.2% accuracy** with perfect recall on class 0
- Key features influencing delivery prediction:
  - **Area**
  - **IsTakeaway**
  - **CuisineCount**

---

##  Model Comparison

- **Logistic Regression**: Fairer predictions across both classes but lower accuracy
- **Random Forest**: Excellent accuracy on majority class but failed to predict minority class

---

##  Conclusion

This project demonstrates the development of a real-world classification pipeline using Zomato data. It highlights the challenges of class imbalance and the trade-offs between fairness and overall accuracy.

Key takeaways:
- Feature engineering plays a crucial role in improving performance
- Class imbalance can heavily bias ML models and requires mitigation
- Visualization and interpretation of results are essential for business understanding

---

##  Technologies Used

- Python 
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Jupyter Notebook


