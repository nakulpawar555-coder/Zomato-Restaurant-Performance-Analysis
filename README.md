# 🍽️ Zomato Restaurant Performance Analysis

**Exploratory data analysis of 148 Zomato restaurants: ratings, customer engagement, pricing and digital adoption, with business decisions for leadership.**

📄 **Full management report:** [Zomato_EDA_Management_Report.pdf](Zomato_EDA_Management_Report.pdf)

---

## 🎯 Objective
Understand how restaurants on Zomato perform across customer engagement, quality perception, pricing and digital adoption, and turn those patterns into concrete decisions for growth, restaurant partnerships and product priorities.

## 📊 Dataset
148 restaurant listings across four categories (Buffet, Cafes, Dining, Other).

| Column | Description |
|---|---|
| `restaurant name` | Name of the restaurant |
| `online_order` | Accepts online orders (Yes/No) |
| `book_table` | Offers table booking (Yes/No) |
| `rate` | Customer rating (out of 5) |
| `votes` | Number of customer votes |
| `approx_cost(for two people)` | Approximate cost for two (₹) |
| `listed_in(type)` | Restaurant type |

## 🧹 Data Preparation
- Converted `rate` from text (e.g. "4.1/5") to a numeric value
- Standardised column names to lower case and renamed the cost column to `approx_cost`
- Checked for missing values (**0**) and duplicate rows (**0**)

## ❓ Business Questions Answered
1. Votes received by each restaurant type
2. Restaurants offering table booking
3. Restaurants with the highest votes
4. Relationship between ratings and votes
5. Average rating by restaurant type
6. Which restaurant type dominates the platform
7. Most common ratings
8. Average cost for two by restaurant type
9. Online vs offline ordering and ratings
10. Restaurant types with more offline-only records

## 🔍 Key Findings

| Metric | Result |
|---|---|
| Dining share of listings | **74%** (110 of 148) |
| Dining share of all votes | **52%** (20,363 of 39,192) |
| Average rating (all restaurants) | **≈ 3.63** |
| Restaurants accepting online orders | **39%** (58 of 148) |
| Restaurants offering table booking | **5.4%** (8 of 148) |

- **Dining is the engine and the weak spot.** It has the lowest average rating (3.57), the lowest cost for two (₹357), the fewest votes per restaurant (185) and only 30% online ordering.
- **Engagement is concentrated.** Empire Restaurant (4,884 votes) and Meghana Foods (4,401 votes) hold about 24% of all votes.
- **Quality is solid but not exceptional.** Ratings cluster between 3.6 and 4.2; only 23% of restaurants score 4.0 or higher and just 3% reach 4.4+.
- **Online-enabled restaurants rate higher** (median ≈ 3.9 vs ≈ 3.4), and 77 of the 90 offline-only restaurants are Dining.
- **Pricing:** Buffet (₹671) and Other (₹669) are premium segments; Dining (₹357) is the value segment.
- **Table booking is almost absent** across the platform.

## 💡 Business Decisions

| # | Decision | Priority |
|---|---|---|
| 1 | Dining online-enablement programme | High |
| 2 | Table-booking rollout in Dining | High |
| 3 | Dining quality-uplift programme | High |
| 4 | "Hidden gems" discovery engine (high-rated, low-vote restaurants) | Medium |
| 5 | Amplify proven top performers | Medium |
| 6 | Segment-specific pricing and promotions | Medium |
| 7 | Strengthen the data foundation (unique IDs, more fields, A/B testing) | Foundation |

## ⚠️ Limitations
- Small, single-snapshot dataset (148 restaurants)
- Votes measure engagement, not order volume or revenue
- The online-vs-rating link is correlation, not causation (Dining is both lower-rated and mostly offline)
- One restaurant (Onesta) appears twice under two categories
- No city, cuisine, date or order-volume fields

## 🛠️ Tech Stack
Python · pandas · NumPy · matplotlib · seaborn · Jupyter Notebook

## 📁 Repository Contents
- `zomatoEDAproject.ipynb`: full analysis notebook
- `Zomato_EDA_Management_Report.pdf`: management report with charts, insights and recommendations
- `ZomatoEDAProject.pptx`: presentation

## ▶️ How to Run
```bash
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook zomatoEDAproject.ipynb
```

