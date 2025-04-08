# 🎮 Video Game Sales Analysis & Prediction

This project explores the **vgchartz-2024.csv** dataset to analyze and predict global video game sales. The analysis investigates how regional sales impact total sales and evaluates the reliability of data across different publishers, while offering insights that can be used for future prediction models.

---

## 📂 Dataset Overview

The dataset, sourced from [Maven Analytics](https://mavenanalytics.io/data-playground), includes detailed sales and metadata for over 64,000 video game titles. Key fields include:

| Field | Description |
|-------|-------------|
| `title` | Game title |
| `console` | Platform the game was released on |
| `genre` | Game genre (e.g., action, shooter) |
| `publisher` | Company that published the game |
| `developer` | Company that developed the game |
| `critic_score` | Metacritic score (out of 10) |
| `total_sales` | Global sales (in millions of copies) |
| `na_sales`, `jp_sales`, `pal_sales`, `other_sales` | Regional sales (in millions) |
| `release_date` | Original release date |
| `last_update` | Date of last dataset update |

---

## 🧪 Methodology

### 1. **Data Loading & Preprocessing**
- Loaded dataset using **Pandas**
- Selected relevant columns for analysis:  
  `title`, `console`, `genre`, `publisher`, `developer`, `total_sales`, and regional sales columns  
- Cleaned and prepared data for further exploration

### 2. **Correlation Analysis**
- Performed **Pearson correlation** analysis between `total_sales` and regional sales
- Identified strong and weak market influences on global performance

### 3. **Missing Data & Error Ratio Analysis**
- Computed an **"error ratio"**: the proportion of games with missing `total_sales` per publisher
- Analyzed this metric against total publisher sales to assess data quality and its potential impact on prediction models

### 4. **Visualization**
- Created histograms and scatter plots to:
  - Visualize distribution of missing data
  - Understand relationship between publisher size and data completeness

---

## 📊 Key Insights

### 🧭 1. **Global Sales are Driven Primarily by NA & PAL Regions**
- **North America** has the highest correlation with global sales (**r = 0.914**), followed by the **PAL region** (**r = 0.907**)
- **Japan** shows a **weak correlation** (**r = 0.212**), highlighting its unique market behavior
- 📌 *Insight*: A game’s success in North America and Europe strongly predicts global performance, whereas Japan tends to follow different sales trends

---

### 📉 2. **Data Completeness Varies by Publisher Size**
- Smaller publishers (e.g., *Nighthawk Interactive*, *Arc System Works*) have **high error ratios**, indicating frequent missing data
- Major publishers (e.g., *Rockstar Games*, *Electronic Arts*, *Activision*) have **very low error ratios**, signifying more reliable data
- 📌 *Insight*: Data completeness is strongly tied to publisher prominence — an important factor when training machine learning models

---

### 📉 3. **Higher Sales Correlate with Lower Error Ratios**
- Publishers with **lower error ratios** tend to also report **higher total sales**
- Scatter plots reveal a **negative correlation** between missing data and commercial success
- 📌 *Insight*: Trusted sales predictions are more feasible for high-performing publishers due to their consistent data

---

### 🏆 4. **Action & Shooter Games Dominate the Market**
- Games like **Grand Theft Auto V** and **Call of Duty: Black Ops III** appear multiple times among top sellers
- These titles are primarily on **PlayStation** and **Xbox** consoles
- 📌 *Insight*: Action/shooter games on mainstream platforms historically drive the majority of global video game sales

---

### ⚠️ 5. **Niche Genres Like Visual Novels Often Lack Sales Data**
- Visual novels (e.g., *XBlaze Lost: Memories*, *Yoru, Tomosu*) frequently have missing or unreported sales
- 📌 *Insight*: Certain genres suffer from underreporting, which may skew analytical models if not properly accounted for

---

## 🛠 Technologies Used

- **Python**
- **Pandas** — for data manipulation  
- **Seaborn** — for data visualization  
- **Scikit-learn** — for regression modeling

---

## 👨‍💻 Author

**Aditya Joshi**  
Student, *National University of Singapore*  
🔗 [LinkedIn: thisisaditya17](https://www.linkedin.com/in/thisisaditya17)  
📧 [joshi.adi1734@gmail.com](mailto:joshi.adi1734@gmail.com)

---

## 🎓 Credits

This project is inspired by a tutorial from the **Dataquest YouTube Channel**:  
🔗 [Watch here](https://www.youtube.com/watch?v=Hr06nSA-qww&t=1777s)

---