# 📊 Amazon Product Rating & Review Sorting

This project analyzes user reviews of an Amazon electronic product to calculate **time-based weighted average ratings** and rank the **most helpful reviews**.  
The goal is to prioritize more recent and reliable reviews to provide better guidance for potential customers.

## 🚀 Project Objective

In e-commerce, product ratings and the order in which reviews are displayed directly influence users' purchasing decisions.  
In this project:

- **Time-based weighted average ratings** are calculated.
- Reviews are scored using:
  - `Up-Down Difference`
  - `Average Rating`
  - `Wilson Lower Bound Score`
- The top 20 most helpful reviews are selected and visualized.

---

## 📁 Dataset

Dataset: `amazon_review.csv`  
- It contains user reviews for a top-reviewed electronic product.
- Key columns:
  - `overall`: Product rating
  - `reviewText`: User review text
  - `helpful_yes`: Number of helpful votes
  - `total_vote`: Total number of votes
  - `day_diff`: Days since the review was written

---

## ⚙️ Methods Used

### 1. Time-Based Weighted Average
Weights are assigned based on the recency of the review, giving more importance to recent reviews.

### 2. Review Scoring Techniques
Three scoring methods are used to rank reviews:

- `score_pos_neg_diff = up - down`
- `score_average_rating = up / (up + down)`
- `wilson_lower_bound`: A confidence-based ranking score

### 3. Visualization
- The top 20 reviews (based on Wilson Lower Bound) are visualized using `Seaborn`.

---

## 🧪 Libraries Used

- `pandas`
- `numpy`
- `scipy`
- `seaborn`
- `matplotlib`

---

## 📌 Conclusion

- Time-based weighted average scoring helps highlight more **recent and relevant reviews**.
- The `Wilson Lower Bound` method ensures **more trustworthy reviews** are prioritized.
- This approach improves both customer satisfaction and the e-commerce platform’s reliability by displaying high-quality feedback.

---
