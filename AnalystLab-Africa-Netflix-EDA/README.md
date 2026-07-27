# Netflix Movies & TV Shows: Data Cleaning & EDA

**Program:** AnalystLab Africa Internship — Week 1-2
**Tools used:** Python (pandas, matplotlib)

## Objective
Clean the Netflix titles catalog and explore content patterns format mix, growth over time,
producing countries, ratings, and genres.

## Dataset
Netflix's catalog of movies and TV shows, including title, director, cast, country, date added,
release year, rating, duration, genre categories, and description. Each row = one title.
Unique identifier: `show_id`.

## Data Cleaning

| Issue Found | Action Taken |
|---|---|
| Missing `director` (2,634), `cast` (825), `country` (831) | Filled with `"Not Specified"` too many rows to drop without losing significant data |
| Missing `date_added` (10), `rating` (4), `duration` (3) | Rows dropped — negligible amount, safe to remove |
| Duplicate rows | 0 found none to remove |
| Inconsistent column names | Standardized to lowercase, no spaces |
| `date_added` stored as text | Converted to proper datetime format |
| Misplaced duration values in `rating` column (e.g. `"74 min"`) | Identified and corrected — moved to `duration`, `rating` set to `"Not Rated"` |

## Key EDA Findings & Insights

1. **Movies dominate the catalog**  Movies (6,131 titles) outnumber TV Shows (2,676) by more
   than 2-to-1, suggesting a catalog strategy favoring standalone films over serialized content.

2. **Content additions grew sharply in recent years**  the number of titles added increased
   substantially through the mid-to-late 2010s, reflecting Netflix's aggressive content
   acquisition phase during its global growth period.

3. **The United States leads content production**  by a wide margin, followed by India and the UK.

4. **Mature content ratings are most common**  TV-MA and TV-14 lead, indicating the catalog
   skews toward teen/adult audiences rather than young children's content.

5. **Dramas and international content dominate genres** International Movies, Dramas, and
   Comedies are the most frequent genre tags, with Independent Movies, Children & Family, and
   Romance also featuring prominently.

## Visualizations
1. Movies vs. TV Shows distribution (pie chart)
2. Content added to Netflix by year (line chart)
3. Top 10 content-producing countries (bar chart)
4. Most common content ratings (bar chart)
5. Most common genres/categories (horizontal bar chart)

## Files in this project
- [`netflix_cleaning_eda.ipynb`](./netflix_cleaning_eda.ipynb) full cleaning, EDA, and visualization code
- [`Netflix_Cleaned.csv`](./Netflix_Cleaned.csv) — cleaned dataset

## Skills applied
`Python` `pandas` `matplotlib` `Data Cleaning` `Data Validation` `Exploratory Data Analysis` `Data Visualization`
