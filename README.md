# Movie Ratings, Genres & Financial Performance Analysis

**Dataset:** [The Movies Dataset – Kaggle](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset)

---

## Project Overview

This project investigates how movie ratings, genres, and budgets relate to financial performance using the `movies_metadata.csv` file from the Kaggle Movies Dataset. By analyzing ~45,000 movies, we aim to uncover insights into what drives ROI and audience approval in the film industry.

<img width="1080" height="1350" alt="image" src="https://github.com/user-attachments/assets/c729fcd8-e819-4201-8bab-1191a8d1d43e" />

---

## Objectives

- Explore the relationship between **weighted movie ratings** and **return on investment (ROI)**
- Analyze the impact of **budget categories** and **genre** on financial performance
- Identify **trends** in ratings and revenue over time
- Detect **rating and ROI outliers** using statistical methods

---

## Dataset Information

- File: `movies_metadata.csv`
- Key columns used:
  - `id`
  - `title`
  - `release_date`
  - `genres`
  - `vote_average`
  - `vote_count`
  - `budget`
  - `revenue`

---

## Data Cleaning & Preprocessing

- Converted numeric columns (`budget`, `revenue`, `vote_count`, `vote_average`) to appropriate types
- Handled missing values and removed rows with zero budget or revenue
- Parsed `genres` column from stringified lists to extract genre names

---

## Key Features Engineered

### ROI Calculation

ROI = (revenue - budget) / budget


## Outlier Analysis: ROI & Rating Over/Underperformers

To identify movies that significantly overperformed or underperformed in terms of ROI and audience ratings, we used Z-score standardization.

### 📈Methodology

- **Z-Score Calculation:**
  - ROI Z-score: `z = (ROI - mean) / std` using `scipy.stats.zscore`
  - Weighted Rating Z-score: same method applied to `weighted_rating`

- **Thresholds:**
  - Z-score > 2: **Overperformers**
  - Z-score < -2: **Underperformers**
 
## Visualization Excerpts

<img width="835" height="573" alt="Screenshot 2025-07-16 at 21 57 44" src="https://github.com/user-attachments/assets/322f9d29-50d8-49f6-924f-71533cc68e4f" />

<img width="482" height="370" alt="Screenshot 2025-07-16 at 21 58 06" src="https://github.com/user-attachments/assets/f274e5fe-1b8a-4f59-bd9f-f528eceb8765" />

<img width="988" height="493" alt="Screenshot 2025-07-16 at 21 57 55" src="https://github.com/user-attachments/assets/c6bd01f6-f0a7-4d23-9284-793ca7e39487" />



