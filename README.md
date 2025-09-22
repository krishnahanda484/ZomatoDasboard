# Metro Data Analysis Dashboard

A Power BI (.pbix) report analyzing metro / public transport data to uncover insights, trends, and recommendations. This repository holds the full report and related artifacts so you and others can explore what was done, how, and why.

---

## 🔗 View the Report

You can download / view the .pbix file here:  
[Metro Data Analysis Report (.pbix)](https://drive.google.com/file/d/14ZGJis02KCXBy4D-b60hd8SdrKw5Yup7/view?usp=sharing)

---

## Table of Contents

1. [Project Overview](#project-overview)  
2. [What I Did](#what-i-did)  
3. [Data Sources & Tools](#data-sources--tools)  
4. [Key Findings & Insights](#key-findings--insights)  
5. [How It Works](#how-it-works)  
6. [Usage](#usage)  
7. [Future Improvements](#future-improvements)  
8. [License](#license)  

---

## Project Overview

This project provides an interactive dashboard that analyzes metro transportation data. My goal was to explore trends, identify bottlenecks, understand passenger behavior, and provide actionable insights to improve operations, efficiency, and user satisfaction.

Key motivations:

- To understand peak usage times, station-level traffic, delays, and patterns.  
- To provide visualizations that are intuitive for both technical and non-technical stakeholders.  
- To enable data-driven decisions for scenario planning (e.g. staffing, schedule adjustments).

---

## What I Did

In this report:

- Cleaned and prepared raw data for analysis (including handling missing values, formatting, aggregation).  
- Built multiple visualizations in Power BI to show:  
  - Station-wise passenger counts over time  
  - Peak vs off-peak usage  
  - Delay / waiting time distributions  
  - Ridership trends (daily / weekly / monthly)  
  - Comparisons between lines (if applicable)  
- Implemented filters and drill-down features (e.g. by date, station, metro line) so users can interact with the data.  
- Designed the dashboard layout for clarity — title / legends / tooltips / color coding to make patterns obvious.  
- Exported and tracked the `.pbix` file in this Git repo (with Git LFS for large file support) so the full report is versioned.

---

## Data Sources & Tools

| Category | Details |
|----------|---------|
| **Data Sources** | *Describe the data you used: for example, CSV logs of metro swipe-ins, delay logs, schedule data, station metadata, etc.* |
| **Tools** | Power BI Desktop (report authoring), Git & Git LFS (version control for large PBIX file), any data cleaning tools (Excel, Python, etc.) if used. |
| **Technologies / Skills** | Data cleaning / ETL, Data visualization, Statistical summarization, Dashboard design, Git version control. |

---

## Key Findings & Insights

Here are some of the most important insights revealed by the analysis:

- **Peak passenger load times:** *E.g., morning rush (7-9 AM) and evening peak (5-7 PM)*  
- **Stations with consistently high traffic:** *E.g., Station A, Station B show very high usage throughout the day*  
- **Delay / waiting time patterns:** *E.g., average delays higher during monsoon months, or during major events*  
- **Ridership trends over time:** *Monthly ridership increasing / decreasing, weekdays vs weekends differences.*  
- **Line comparisons:** *If one line is under-utilized or overcrowded compared to others.*  

These findings can help decision makers plan resource allocation, optimize schedules, improve passenger experience, etc.

---

## How It Works

Here’s a brief on how the dashboard works under the hood:

1. **Data Ingestion:** Raw data files are loaded into Power BI.  
2. **Data Preparation / Transformation:** Cleaning steps such as: removing nulls, standardizing date/time formats, aggregating data by station / line / date.  
3. **Modeling:** Creating relationships if multiple tables; creating measures (e.g. total passengers, average delay).  
4. **Visualization:** Multiple visuals (bar charts, line charts, heat maps, etc.), filters / slicers so users can interact.  
5. **Version Control:** The `.pbix` file is large, so I used Git Large File Storage (LFS) to properly version it without bloating the repo.

---

## Usage

To use this repository / report:

- Clone the repository:  
  ```bash
  git clone git@github.com:krishnahanda484/ZomatoDasboard.git
