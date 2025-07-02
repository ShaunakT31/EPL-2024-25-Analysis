# Premier League 2024/25: In-Depth Player and Team Performance Analysis

Comprehensive data analysis of the Premier League 2024/25 season using Python. The project includes web scraping, performance profiling, player efficiency evaluation, team dependency assessment, and tactical build-up analysis using advanced football metrics such as xG, xA, xGChain, and xGBuildup.

---


## Table of Contents

- [Project Overview](#project-overview)
- [Project Structure](#project-structure)
- [Tools and Libraries Used](#tools-and-libraries-used)
- [Dataset and Data Collection](#dataset-and-data-collection)
- [Problem Statements](#problem-statements)
  - [1. Player Value Analysis (xG + xA per 90)](#1-player-value-analysis-xg--xa-per-90)
  - [2. Player Efficiency and Shot Profiles](#2-player-efficiency-and-shot-profiles)
  - [3. Team Dependency on Star Players](#3-team-dependency-on-star-players)
  - [4. Team Build-Up and Progression Profiles](#4-team-build-up-and-progression-profiles)
- [Key Insights](#key-insights)
- [How to Run](#how-to-run)
- [Conclusions](#conclusions)
- [Contact](#contact)

---


## Project Overview

This project provides a detailed, data-driven analysis of the English Premier League (EPL) 2024/25 season. The primary objective is to uncover actionable insights into player performance, team strategies, and offensive dynamics using advanced football statistics.

The analysis was performed using data scraped from **Understat**, a trusted source for football metrics and data.

The project is divided into four key analytical modules:
1. **Player Performance & Value Analysis** – Identifying the most valuable players based on xG and xA per 90 minutes.
2. **Player Efficiency and Shot Profiles** – Evaluating shooting efficiency, shot volume, and all-round offensive influence.
3. **Team Dependency on Star Players** – Analyzing the extent to which teams rely on key players for goal contributions.
4. **Team Build-Up and Progression Profiles** – Understanding team tactics, build-up patterns, and ball progression styles.

Each module includes well-structured visualizations and player/team rankings to support meaningful football insights.

---


## Project Structure

```text
project-root/
│
├── EPL_UnderStat_Scraper.ipynb                # Web scraping notebook to extract Premier League player data from Understat
├── EPL_2024_25_Player_Performance.ipynb       # Analysis 1: Player Value based on xG + xA per 90
├── EPL_2024_25_Player_Efficiency.ipynb        # Analysis 2: Player Efficiency and Shot Profiles
├── EPL_2024_25_Player_Dependencies.ipynb      # Analysis 3: Team Dependency on Star Players
├── EPL_2024_25_Team_Playstyles.ipynb          # Analysis 4: Team Build-Up and Progression Profiles
├── README.md                                  # Project overview, methodology, insights, and instructions
└── premier_league_2024_25.csv                 # Cleaned dataset containing player statistics for the 2024/25 season
```


Each Jupyter Notebook is self-contained with code, visualizations, and detailed markdown explanations for reproducibility and independent review.

---


## Tools and Libraries Used

The following tools and libraries were used to develop and analyze this project:

- **Python 3.11**: Core programming language used for data scraping, processing, and analysis.
- **Jupyter Notebook**: Interactive development environment used to build, visualize, and document each step of the analysis.
- **asyncio**: To handle asynchronous operations during web scraping.
- **aiohttp**: For making asynchronous HTTP requests to scrape data.
- **nest_asyncio**: Allows nested event loops to run asynchronous code seamlessly within Jupyter.
- **Understat**: Python package used to scrape detailed player and team statistics from the Understat website.
- **pandas**: For data manipulation, aggregation, and preprocessing.
- **numpy**: For numerical computations and efficiency in data handling.
- **matplotlib**: For static visualizations and plotting.
- **seaborn**: For advanced statistical data visualizations.
- **plotly.express**: For creating interactive plots and scatter visualizations.
- **plotly.graph_objects**: For enhanced customization of Plotly charts and detailed layout control.

---


## Dataset and Data Collection

The dataset for this project was self-collected using a **custom-built Python web scraper** that extracted detailed player statistics from the [Understat](https://understat.com/) website for the **Premier League 2024/25 season**.

### Dataset Columns

| Column Name               | Description                                      |
|---------------------------|--------------------------------------------------|
| Player                    | Player's name                                    |
| Team                      | Player's team                                    |
| Games                     | Matches played                                   |
| Minutes Played            | Total minutes played                             |
| Goals                     | Goals scored                                     |
| Assists                   | Assists provided                                 |
| Shots                     | Total shots attempted                            |
| xG                        | Expected goals                                   |
| xA                        | Expected assists                                 |
| xG Chain                  | Total xG from sequences the player was involved in|
| xG Buildup                | Total xG from sequences without shots/key passes  |
| Key Passes                | Passes leading directly to shots                 |
| Position                  | Player’s primary and secondary positions         |

Additional derived metrics were calculated in the notebooks:
- xG per 90
- xA per 90
- xG + xA per 90
- Goals per Shot
- Key Passes per 90
- Shots per 90
- xG per Shot
- Total Offensive Contribution per 90
- Goal Contribution % per Team
- Assist Contribution % per Team
- Key Pass Contribution % per Team
- xGChain per 90
- xGBuildup per 90

---


### Dataset Details:
- The cleaned dataset used for all analyses is provided in this repository as:
  
  **`EPL_2024_25_Understat.csv`**

> **Note:** The scraping process was conducted solely for educational purposes and adheres to the fair usage policies of the data source.

---


## Problem Statements

This project addresses four distinct but interconnected football analytics problems using data from the Premier League 2024/25 season. Each analysis provides unique perspectives on player performance, team strategies, and ball progression.

---


## 1. Player Performance & Value Analysis (xG + xA per 90)

### Objective
Identify the most valuable players based on their expected goal (xG) and expected assist (xA) contributions per 90 minutes.

### Key Questions
- Who are the most impactful players when normalized per 90 minutes?
- Which players overperformed or underperformed relative to their expected contributions?
- How can we identify players whose goal and assist counts do not fully reflect their underlying impact?

---


## 2. Player Efficiency and Shot Profiles

### Objective
Develop detailed efficiency and shot profiles for Premier League players by analyzing shot volume, shot quality, and offensive influence.

### Key Questions
- Which players were the most clinical finishers (highest goals per shot)?
- Which players were the most frequent shooters and most influential chance creators?
- Can players be classified as clinical, volume shooters, or all-round offensive contributors?

---


## 3. Team Dependency on Star Players

### Objective
Examine the degree to which teams rely on key individuals for their attacking output.

### Key Questions
- Which players contribute the highest proportion of their team’s goals, assists, and key passes?
- Which teams are heavily dependent on one or two players?
- Which teams display a balanced distribution of offensive responsibilities?

---


## 4. Team Build-Up and Progression Profiles

### Objective
Analyze how Premier League teams build their attacks and progress the ball through different phases.

### Key Questions
- Which teams rely on structured build-up play versus direct attacking transitions?
- Which teams rank highest in xGChain and xGBuildup per 90?
- Which players are key build-up contributors, often involved in deeper phases of play?

---


## Key Insights

Throughout this project, several important trends and actionable insights emerged from the detailed analyses:

- **Per 90 Normalization is Critical:** Evaluating player contributions on a per 90-minute basis allowed for fair comparisons regardless of total minutes played, ensuring that impact substitutes and less frequently used players were not overlooked.

- **Overperformance and Underperformance Patterns:** Some players consistently exceeded their expected goal and assist outputs, indicating elite finishing, strong positional awareness, or exceptional form. Conversely, underperformers highlighted potential issues with shot quality, decision-making, or simply variance that could stabilize over time.

- **Player Efficiency Profiling:** Players can be meaningfully classified into clinical finishers, volume shooters, and all-round contributors. This provides valuable information for scouting, tactical planning, and performance evaluation.

- **Team Dependency on Key Individuals:** Certain teams were heavily reliant on their top players for attacking production, while others demonstrated a more balanced distribution. Identifying these dependencies offers insight into potential team vulnerabilities and the tactical flexibility of each squad.

- **Build-Up and Progression Diversity:** The xGChain and xGBuildup metrics revealed stylistic differences between teams. Some clubs emphasized patient, possession-based progression involving multiple players, while others favored quicker, more direct attacking transitions.

- **Positional Influence on Build-Up:** Midfielders and versatile players (operating across multiple positions) emerged as the most influential in build-up phases, while forwards primarily drove direct offensive contributions.

These insights collectively contribute to a more nuanced understanding of player impact, team strategies, and tactical tendencies in the Premier League 2024/25 season.

---


## How to Run

To run this project locally:

1. Clone the repository:
    ```bash
    git clone <repository-link>
    ```
2. Ensure you have Python 3.11 installed with the required libraries:
    ```bash
    pip install pandas numpy matplotlib seaborn plotly aiohttp nest_asyncio understat
    ```
3. Run the Jupyter notebooks:
    - `EPL_UnderStat_Scraper.ipynb` (to scrape the data)
    - `EPL_2024_25_Player_Performance.ipynb`
    - `EPL_2024_25_Player_Efficiency.ipynb`
    - `EPL_2024_25_Player_Dependencies.ipynb`
    - `EPL_2024_25_Team_Playstyles.ipynb`

---


## Conclusions

This project provided a multi-dimensional performance evaluation of Premier League players and teams for the 2024/25 season using modern football analytics.

### Key Outcomes:
- Identification of high-value players beyond raw goal and assist counts.
- Classification of players into clinical finishers, volume shooters, and efficient creators.
- Quantification of team reliance on star players versus collective offensive strategies.
- Detailed team build-up profiles highlighting possession-oriented versus direct play styles.

This project showcases the importance of using expected metrics and per 90-minute normalizations to develop balanced, insightful evaluations of player and team performance.

---


## Contact

For questions, collaborations, or feedback:

**Shaunak Torgatti**  
Email: shaunakht@gmail.com  
LinkedIn: [www.linkedin.com/in/shaunaktorgatti](https://www.linkedin.com/in/shaunaktorgatti)

---
