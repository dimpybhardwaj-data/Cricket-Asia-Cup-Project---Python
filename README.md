🏏 Cricket Asia Cup Data Analysis

📌 Project Overview
This project analyzes Asia Cup cricket matches using Python and Pandas.
The dataset contains 254 matches with 20 columns of match statistics (runs, wickets, toss results, venues, player awards, etc.).

The goal is to uncover team‑level, player‑level, and match‑level insights — answering questions like:

- Which team has the highest win percentage?
- Does batting first or bowling first matter?
- How much impact do extras have on match outcomes?
- Which venues are high‑scoring vs low‑scoring?
- Who are the most consistent “Player of the Match” winners?

⚙️ Libraries Used
 - pandas → data cleaning, grouping, aggregation
 - numpy → numerical operations, correlation matrix
 - matplotlib.pyplot → plotting bar charts, win percentages, venue analysis
 - seaborn → correlation heatmaps for performance metrics
 - ipywidgets & IPython.display → interactive notebook display (optional)

🧹 Data Cleaning Steps
- Loaded dataset (asiacup.csv) → 254 rows × 20 columns.
- Checked missing values → handled with dropna() for clean analysis.
- Removed duplicates → df.duplicated().sum().
- Converted categorical columns (Team, Opponent, Format, Ground, etc.) to category type for efficiency.
- Converted Year to datetime.
- Standardized text values (Result, Toss) → stripped spaces, converted to title case.
- Replaced D/L outcomes (Win D/L, Lose D/L) with normal Win/Lose.
- Renamed columns to snake_case for readability (e.g., Run Scored → runs_scored).

📊 Analysis & Insights
1️. Average Score per Innings by Format
ODI: ~217 runs
T20I: ~138 runs
👉 ODI matches are naturally higher scoring than T20Is.

2️. Close Margins vs One‑Sided Wins
Defined margin by wickets lost.
Close Match: 5–8 wickets lost.
One‑Sided Win: fewer wickets lost.
👉 Majority of matches are one‑sided, but close finishes still form a significant share.

3️. High‑Scoring vs Low‑Scoring Venues
Median threshold ≈ 197 runs.
High‑scoring venues: Fatullah, Lahore, Karachi, Dambulla, Abu Dhabi.
Low‑scoring venues: Cuttack, Mirpur, Dubai(DSC), Chandigarh, Sharjah.
👉 Venue conditions strongly influence match totals.

4️. Fours & Sixes Distribution
Average fours per match: 15.6
Average sixes per match: 2.9
Average total boundaries: 18.5
👉 Fours dominate scoring compared to sixes.

5️. Extras Impact on Match Outcomes
Categorized extras into Low, Medium, High, Very High.
Win rates:
Low → 51%
Medium → 45%
High → 57%
Very High → 50%
👉 Moderate extras hurt win chances, but surprisingly, some high‑extras matches still ended in wins.

6️. Toss Impact
Win % after winning toss: 58%
Win % after losing toss: 41%  
👉 Toss has a significant impact (difference ~17%).

7️. Team Win Percentage
India → 67.2% (highest)
Sri Lanka → 66.7%
Pakistan → 57.4%
Afghanistan → 35.7%
Bangladesh → 20%
👉 India and Sri Lanka are the most successful Asia Cup teams.

8️. Batting First vs Bowling First
Batting first win rate → 45.6%
Bowling first win rate → 54.4%
👉 Teams win more often when bowling first.

9️. Best Team at Each Ground
Example highlights:
Sharjah → India
Colombo(RPS) → Sri Lanka
Dubai(DSC) → India
Dhaka → Pakistan
👉 Different teams dominate at different venues.

10. Highest Average Runs per Team
Pakistan → 217.6
India → 213.7
Sri Lanka → 212.6
👉 Pakistan edges out India and Sri Lanka in average runs per match.

11. Defensive Performance
Calculated runs conceded using opponent’s runs.
Found the team that concedes the fewest runs per match (best defense).

12. Player Insights
Most Player of the Match awards → Surinder Khanna, Roy Dias, Wasim Akram, etc.
Top award winners by team, ground, and year.
Consistency analysis → players who won across multiple years.
Impact analysis → teams usually win when their player gets the award.

13. Correlation Analysis
Added total_boundaries column.
Heatmap showed:
Strong positive correlation between fours_hit & run_rate (0.96).
Negative correlation between wickets_lost & avg_bat_strike_rate (-0.52).
👉 Boundaries and strike rate drive scoring, while losing wickets drags performance down.

📈 Visualizations
Correlation Heatmap → relationships between runs, wickets, boundaries, strike rate.
Bar Charts → win percentage by team, toss impact, batting vs bowling wins.
Venue Analysis → high vs low scoring grounds.
Best Team per Ground → bar plot with win percentages.

✅ Final Data Quality Report
Records: 254
Columns: 20
Missing values: 0 (after cleaning)
Duplicate rows: 0
Date range: 1984 → 2022
Teams: 7 (India, Pakistan, Sri Lanka, Bangladesh, Afghanistan, Hong Kong, UAE)

💾 Output
Cleaned dataset saved as: cricket_data_cleaned.csv
All insights reproducible via Jupyter Notebook.

🚀 Conclusion
This project demonstrates how data science + cricket statistics can uncover meaningful insights:
- Toss and bowling first matter.
- India & Sri Lanka dominate overall.
- Venues strongly influence scoring.
- Extras and boundaries shape match outcomes.
- Player awards align with team success.

It’s a complete sports analytics case study using Python, Pandas, and visualization libraries.
