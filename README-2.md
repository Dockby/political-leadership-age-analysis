# Does Leader Age Actually Matter? A Data Analysis of 177 Countries (1989–2020)

I've always been curious about whether the age of a political leader actually changes how a country is run. You hear a lot of opinions about this — older leaders are more stable, younger ones are reckless, or the opposite. I wanted to see what the data actually says.

So I pulled together data on 1,109 world leaders across 177 countries from 1989 to 2020, merged it with World Bank spending indicators, and ran the numbers. Some of what I found confirmed my expectations. A lot of it didn't.

---

## What I Was Trying to Find Out

- Do younger leaders hold power longer or shorter than older ones?
- Do older leaders really spend more on the military?
- Does gender affect spending priorities?
- Which regions tend to produce younger leaders vs older ones?

---

## Datasets Used

- **PLAD (Political Leaders' Affiliation Database)** — 1,109 leaders, 177 countries, 1989–2020. Includes birth year, entry/exit dates, gender, education level.
- **World Bank — Military Expenditure (% of GDP)**
- **World Bank — Government Expenditure on Education (% of GDP)**
- **World Bank — Current Health Expenditure (% of GDP)**

I merged all four datasets by matching country and year, expanding each leader's tenure into individual years so I could link spending data to the exact years they were in power.

---

## Key Findings

### 1. Young leaders stay in power significantly longer

| Age Group | Avg. Years in Power |
|---|---|
| Young (Under 45) | 8.84 |
| Middle-aged (45–59) | 5.00 |
| Senior (60+) | 3.53 |

This was the most surprising result. I expected senior leaders to be more entrenched, but the data says the opposite. Young leaders — who are rarer to begin with (only 18% of all leadership periods) — tend to hold on much longer once they get in.

A t-test confirmed this isn't random chance: **t-statistic = 8.56, p-value < 0.0001.**

### 2. My hypothesis about military spending was wrong

I assumed older leaders would spend more on the military. The data doesn't really support that. Spending patterns across age groups are surprisingly similar. If anything, middle-aged leaders spend the *least* on military (2.02% of GDP vs ~2.50% for both younger and older groups).

The more interesting finding came from gender.

### 3. Female leaders spend less on military, more on health

| Gender | Military (% GDP) | Education (% GDP) | Health (% GDP) |
|---|---|---|---|
| Female | 1.72 | 4.51 | 6.83 |
| Male | 2.31 | 4.36 | 5.95 |

Female leaders allocate about 25% less to military spending and noticeably more to healthcare. This held up consistently across the dataset.

### 4. Regional patterns in leadership age

Europe has the highest proportion of young leaders by a significant margin. Asia skews heavily toward senior leadership. Africa and the Americas are dominated by middle-aged leaders. This suggests that political culture and institutional norms shape who gets to lead — not just individual merit or circumstance.

### 5. Education level doesn't vary much by age group

All three groups averaged between 7 and 8 on the education scale (Masters-level and above). Being highly educated seems to be a baseline requirement for political leadership regardless of age.

---

## A Note on Data Limitations

World Bank spending data wasn't available for all countries in all years — particularly for conflict-affected states in the early 1990s. I worked with ~4,500 data points for military and ~3,300–3,500 for education and health out of 7,900 total leader-year observations. The findings are directionally solid but should be read with that context in mind.

---

## Tools Used

- Python (Pandas, NumPy, Matplotlib, Seaborn, SciPy)
- Google Colab
- Data sources: PLAD Database, World Bank Open Data

---

## Files

- `political_leadership_age_analysis.ipynb` — full analysis notebook
- `PLAD_Oct_2021.csv` — leaders dataset
- World Bank CSVs for military, education, and health expenditure

---

*Chetan Singh | B.Tech Computer Science (2022–2026)*
