# Experiment 1: EDA in IPL Dataset
## Reg no:212224240134
## Aim:
To perform Exploratory Data Analysis (EDA) on the IPL matches dataset and derive insights about matches per season, winning teams, toss decisions, and top venues.

## Algorithm / Procedure:

## 1.Import Libraries
  Import pandas for data handling.
  Import matplotlib and seaborn for visualization.
## 2.Load Dataset
  Use pd.read_csv() to load the IPL matches dataset.
  Check dataset shape using .shape.
  View first 5 rows using .head().
## 3.Matches per Season (Univariate Analysis)
  Group data by season and count matches.
  Plot a bar chart to visualize growth/decline in matches.
## 4.Top Winning Teams (Univariate Analysis)
  Use value_counts() on the winner column.
  Plot top 5 winning teams in a bar chart.
## 5.Toss Decisions (Univariate Analysis)
  Count toss decision preferences (bat vs field).
  Plot results using a bar chart.
## 6.Top Venues (Univariate Analysis)
  Count matches per venue.
  Display top 5 venues with a horizontal bar chart.
## 7.Draw Insights
  Observe patterns in toss decisions.
  Identify teams with consistent winning trends.
  
  ## Program:

### Basic info about dataset:
```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
matches = pd.read_csv("matches.csv")
print("Dataset Shape:", matches.shape)  
print(matches.head())

```
### Matches per season:
```python
 season_counts = matches['season'].value_counts().sort_index()
 print("\nMatches per season:\n", season_counts)
```
### Matches per season plotted:
```python
plt.figure(figsize=(8,4))
sns.barplot(x=season_counts.index, y=season_counts.values, palette="viridis")
plt.title("Number of Matches per Season")
plt.xlabel("Season")
plt.ylabel("Matches")
plt.show()
```

###  Most successful teams:
```python
team_wins = matches['winner'].value_counts()
print("\nTop Winning Teams:\n", team_wins.head(5))

 plt.figure(figsize=(8,4))
 sns.barplot(x=team_wins.head(5).index, y=team_wins.head(5).values, palette="magma")
 plt.title("Top 5 Winning Teams")
 plt.xlabel("Team")
 plt.ylabel("Wins")
 plt.show()
```

###  Toss decisions (bat vs field)
```python
 toss_decision = matches['toss_decision'].value_counts()
 print("\nToss Decisions:\n", toss_decision)

 plt.figure(figsize=(6,4))
 sns.barplot(x=toss_decision.index, y=toss_decision.values, palette="Set2")
 plt.title("Toss Decisions (Bat or Field)")
 plt.show()
```

### Venues hosting most matches:
```python
 venue_counts = matches['venue'].value_counts().head(5)
 print("\nTop Venues:\n", venue_counts)

 plt.figure(figsize=(8,4))
 sns.barplot(y=venue_counts.index, x=venue_counts.values, palette="coolwarm")
 plt.title("Top 5 Venues by Matches Hosted")
 plt.xlabel("Matches Hosted")
 plt.ylabel("Venue")
 plt.show()
```

  ## Output:
### Basic info about dataset:
  <img width="840" height="693" alt="Screenshot 2025-09-01 234821" src="https://github.com/user-attachments/assets/ba7cd5c9-c79e-452a-9024-2d8a769c13cd" />

### Matches per season:
<img width="623" height="421" alt="Screenshot 2025-09-01 235233" src="https://github.com/user-attachments/assets/e670fc52-e235-47d2-9b2e-d2186580d9f4" />

### Matches per season plotted:

<img width="884" height="553" alt="Screenshot 2025-09-01 235419" src="https://github.com/user-attachments/assets/ba954b30-86df-48a3-954d-83ef5c542a62" />

###  Most successful teams:

<img width="487" height="217" alt="Screenshot 2025-09-01 235828" src="https://github.com/user-attachments/assets/c2ff6800-0f2f-4379-aae7-e5ee74f45250" />

<img width="890" height="573" alt="Screenshot 2025-09-01 235929" src="https://github.com/user-attachments/assets/b784ac4f-7226-4b1b-b598-c09f583dbe03" />


###  Toss decisions (bat vs field)

<img width="432" height="153" alt="Screenshot 2025-09-02 000047" src="https://github.com/user-attachments/assets/26249b9c-0976-4801-ab45-a9385be2cca5" />

<img width="877" height="562" alt="Screenshot 2025-09-02 000057" src="https://github.com/user-attachments/assets/184af14d-231c-4abc-add6-d7089e6bf80b" />

### Venues hosting most matches:

<img width="662" height="216" alt="Screenshot 2025-09-02 000241" src="https://github.com/user-attachments/assets/1c2ac118-afb7-4378-b5b5-c10399f69098" />

<img width="901" height="457" alt="Screenshot 2025-09-02 000252" src="https://github.com/user-attachments/assets/4907515c-19d2-4216-9206-72a20fb17edb" />



 ## Result:
  Thus experiment is executed successfully




