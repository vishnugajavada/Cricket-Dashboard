# Cricket-Dashboard
An interactive Power BI dashboard that analyzes cricket match data to visualize player and team performance, track key metrics like runs and wickets, and identify winning trends. It helps users gain actionable insights and make data-driven decisions through clear, dynamic visualizations.

# 🏏 Cricket Match Performance Dashboard

A Power BI analytics dashboard for ICC Champions Trophy — featuring match results, player stats, and team comparisons across all tournament editions.

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![DAX](https://img.shields.io/badge/DAX-217346?style=for-the-badge&logo=microsoft&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-1D6F42?style=for-the-badge&logo=microsoftexcel&logoColor=white)

---

## 📖 Overview

This project visualizes historical **ICC Champions Trophy** data covering match results, player performance, team rankings, and win/loss ratios across all tournament editions. Built in **Power BI** with Python-preprocessed data and SQL-extracted records, the dashboard lets coaches, analysts, and fans interactively explore cricket statistics at a glance.

> 📅 Data spans **1998 to 2017** — covering **116 matches**, **1036 players**, and **13 nations**.

---

## ✨ Features

- 📊 **Interactive Match Analysis** — filter results by team, year, ground, and match type
- 🏆 **Tournament-Wide Stats** — Player of the Match records, margins, and winning patterns
- 🌍 **Team Comparison** — head-to-head W/L ratios, batting & bowling rankings per match
- 🎌 **Team Flag Visuals** — live flag images for all 13 participating nations
- ⚡ **Precomputed Data Model** — optimized for fast slicer response with no lag
- 🧹 **Clean Data Pipeline** — Python-preprocessed CSVs with no missing values or duplicates

---

## 🛠️ Tech Stack

| Tool / Technology | Purpose |
|---|---|
| Power BI Desktop | Dashboard design, DAX measures, interactive visualizations |
| Python 3.x | Data preprocessing, cleaning, and pipeline automation |
| SQL | Data extraction and filtering from relational databases |
| Microsoft Excel / CSV | Raw data storage and structured input files |
| DAX (Data Analysis Expressions) | Custom calculated measures and KPIs in Power BI |

---

## 📁 Project Structure

```
Cricket-Dashboard/
│
├── CA_prac_DB.pbix                                  # Main Power BI dashboard file
│
├── data/
│   ├── all_champions_trophy_matches_results.csv     # Match data (116 records, 19 columns)
│   ├── all_champions_trophy_players_list.csv        # Player list (1036 records)
│   └── team_flags.csv                               # Team flags & board names (13 nations)
│
├── assets/
│   ├── Champion-Trophy.jpg                          # Trophy image used in dashboard
│   └── 1.jpg                                        # Additional image asset
│
└── README.md
```

---

## ⚙️ How It Works

### 1. Data Collection
Match metadata was gathered including team names, toss results, winners, Player of the Match, margins, venues, ODI match numbers, batting/bowling rankings, and head-to-head W/L ratios.

### 2. Data Preprocessing (Python)
- Handled missing values and normalized inconsistent entries
- Standardized date formats across all match records
- Removed duplicate rows to ensure clean, reliable data
- Exported cleaned CSVs for direct import into Power BI

### 3. Loading Data into Power BI
Cleaned CSV files were connected directly to Power BI. Relationships were built between match results, player lists, and team flag tables to create a unified data model.

### 4. Visualizations Designed
- **Bar Chart** — Wins per team across tournament editions
- **Line Chart** — Performance trends across years
- **Table** — Top Player of the Match recipients
- **Clustered Chart** — Team batting vs bowling rankings

### 5. Dynamic Filters (Slicers)
Users can interactively filter the entire dashboard by:
- **Team** — focus on a specific nation's performance
- **Year / Edition** — drill down to a specific tournament
- **Match Ground** — analyze venue-specific results
- **Player** — track individual Player of the Match history

### 6. Custom DAX Measures

```dax
-- Win/Loss Ratio
WinLossRatio = DIVIDE(COUNT(Wins), COUNT(Losses))

-- Average Batting Ranking per Match
AvgBattingRank = AVERAGE(MatchStats[Team1 Avg Batting Ranking])

-- Total Matches Played
TotalMatches = COUNTROWS(MatchResults)
```

---

## 📊 Dataset Summary

| File | Records | Key Columns |
|---|---|---|
| `matches_results.csv` | 116 matches | Team1, Team2, Winner, Player of Match, Margin, Ground, Date |
| `players_list.csv` | 1036 players | Team, Year, Player Name |
| `team_flags.csv` | 13 nations | Team Name, Flag URL, Cricket Board |

---

## 🚀 Getting Started

### Prerequisites
- [Power BI Desktop](https://powerbi.microsoft.com/desktop/) — free download
- Git — for cloning the repository

### Installation

```bash
# Clone the repository
git clone https://github.com/vishnugajavada/Cricket-Dashboard.git
cd Cricket-Dashboard
```

### Open the Dashboard

```bash
# Double-click the .pbix file OR open via Power BI Desktop
CA_prac_DB.pbix
```

### Explore
- Use **slicers** on the panel to filter by team, year, or player
- **Hover** over charts for detailed tooltips
- **Click** any visual to cross-filter the entire dashboard

---

## 📸 Screenshots

> 🖼️ *Screenshots coming soon — open `CA_prac_DB.pbix` in Power BI Desktop to explore.*

---

## 🚧 Known Limitations

- Dataset covers Champions Trophy only (1998–2017) — not other ICC tournaments
- No live data feed — manual CSV update required for new match data
- Player stats limited to Player of the Match — no full batting/bowling scorecards

---

## 🔮 Future Improvements

- [ ] Add live data integration via cricapi.com or ESPN Cricinfo
- [ ] Expand to cover World Cup, IPL, and T20I tournaments
- [ ] Include full player batting and bowling scorecards
- [ ] Publish dashboard to Power BI Service for web access
- [ ] Add predictive win probability using machine learning

---

## 👤 Author

**Gajavada Vishnu**
M.Tech Integrated Software Engineering — VIT Vellore (2021–2026)

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)](https://github.com/vishnugajavada)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/vishnu-gajavada-380631279/)
