# Social Media Descriptive Statistics - 2024 US Presidential Candidates

This project is part of the iSchool, Syracuse University Research. The goal is to provide basic descriptive statistics and grouped summaries for social media activity by political candidates during the 2024 U.S. presidential election.

---

## 📁 Files and Folders

- `data/` – This folder contains the 3 datasets provided (not included in GitHub).
  - `facebook_ads.csv`
  - `facebook_posts.csv`
  - `twitter_posts.csv`
- `pure_python_stats.py` – Script using basic Python (no libraries) for stats.
- `pandas_stats.py` – Script using the Pandas library.
- `polars_stats.py` – Script using the Polars library.
- `visualizations.py` – Script to create visualizations like bar charts, boxplots, and histograms.
- `.gitignore` – Prevents committing datasets and unnecessary files.
- `README.md` – This file.

---

## ⚙️ How to Run

### 1. Set up the environment

```bash
python3 -m venv .venv
source .venv/bin/activate


2. Install required packages
pip install pandas polars matplotlib seaborn

3. Run the scripts
python pure_python_stats.py
python pandas_stats.py
python polars_stats.py
python visualizations.py


🔍 What Each Script Does
pure_python_stats.py: Uses only built-in Python to read the CSV, calculate averages, counts, and frequencies. Good for learning how stats work under the hood.
pandas_stats.py: Uses the Pandas library to calculate .describe(), groupby stats, and frequent values. Fast and widely used in real projects.
polars_stats.py: Uses the Polars library, which is faster for large datasets. Also uses groupby and summary functions.
visualizations.py: Generates visualizations using matplotlib and seaborn. Includes bar charts, histograms, and boxplots.

## Sample Output Screenshots

### Pure Python Script Output
![Pure Python](assets/pure_python.png)

### Pandas Script Output
![Pandas Output](assets/pandas.png)

### Polars Script Output
![Polars Output](assets/polars.png)


🔍 Summary of Findings
While working with the Facebook ads dataset, I noticed some interesting patterns:

The most frequent ad creation date was 2024-10-27, with over 8600 ads created on that single day.

The candidate “HARRIS FOR PRESIDENT” showed up the most in the bylines field — nearly 50,000 times.

Almost all ads used USD as the currency — only a handful used something else.

The most common estimated audience size was 1,000,001, which showed up over 100,000 times.

A large number of ads were shown on both Facebook and Instagram platforms — around 214,000 entries had both.

Some fields like delivery_by_region and demographic_distribution had lots of {} entries, meaning those fields were empty for many ads.

I also saw that mentions and other message-related columns often had blank or zero values — like illuminating_mentions, which had [] in over 73,000 ads.

I tested this with three scripts:

The Pure Python version worked and gave me a basic feel of how to calculate stats manually.

The Pandas script was much quicker and more detailed — especially helpful for grouping and getting summaries.

The Polars script was very fast, but I ran into a .groupby error since Polars handles it differently than Pandas.

This exercise helped me understand how different tools (like Pandas and Polars) handle large datasets and how to extract meaningful insights from structured ad data.


## 📊 Visualization Samples

These charts help communicate the patterns we observed in the data.
Visualizations were created using the visualizations.py script with Seaborn and Matplotlib.

### Top 10 Mentioned Bylines
![Top Bylines](assets/byline_bar.png)

### Estimated Spend Distribution
![Spend Histogram](assets/spend_hist.png)

### Boxplot of Estimated Impressions
![Impressions Boxplot](assets/impressions_box.png)
