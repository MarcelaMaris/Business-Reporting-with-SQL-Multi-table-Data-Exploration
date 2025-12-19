<p align="center">
  <img src="cover_SQL.png" width="100%" alt="E-Commerce Analytics Dashboard cover">
</p>

## <img src="icons/business.png" width="50">  &nbsp;&nbsp;Business Reporting with SQL — Books, Ratings & Reader Behaviour
<br>

![Python](https://img.shields.io/badge/Python-3.10%2B-0A3756?style=flat&logo=python&logoColor=F5F7FA&labelColor=E8AA3A)
![SQL](https://img.shields.io/badge/SQL-SQLite-0A3756?style=flat&logo=sqlite&logoColor=F5F7FA&labelColor=E8AA3A)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-0A3756?style=flat&logo=jupyter&logoColor=F5F7FA&labelColor=E8AA3A)
![Relational](https://img.shields.io/badge/Data-Relational%20Tables-0A3756?style=flat&logo=databricks&logoColor=F5F7FA&labelColor=E8AA3A)
![Insights](https://img.shields.io/badge/Analysis-Product%20Insights-0A3756?style=flat&logo=googleanalytics&logoColor=F5F7FA&labelColor=E8AA3A)

> This project explores a **multi-table book platform database** using **SQL** to extract insights about  
> **catalogue composition, reader behaviour, ratings, authors and publishers**.
>
> The analysis mirrors a **business reporting workflow**, where SQL is used to answer strategic questions that can guide  
> the development of a **new digital product for readers** (recommendations, editorial highlights, and community features).
>
> To ensure full reproducibility on GitHub, the project recreates the database locally using **CSV snapshots** and an  
> **in-memory SQLite engine**, preserving the original SQL logic without requiring database credentials.

💻 **Repository:** https://github.com/MarcelaMaris/Business-Reporting-with-SQL-Multi-table-Data-Exploration

---

## <img src="icons/objectives.png" width="30">  &nbsp;&nbsp;Objectives

- Analyse a **relational dataset** covering books, authors, publishers, ratings, and reviews.
- Validate schema integrity (primary keys, joins, orphan checks) before extracting insights.
- Use **SQL queries** to answer product and business questions (recency, popularity, quality, engagement).
- Identify **high-performing authors and publishers** using volume-aware metrics.
- Translate findings into **recommendation and product strategy ideas** for a reader-focused app.

---

## <img src="icons/features.png" width="30">  &nbsp;&nbsp;Key Analyses & Features

- **Schema & Data Quality Validation:**  
  Table previews, data types, null checks, primary-key uniqueness, orphan detection.

- **Catalogue Recency:**  
  Count of books published after 2000 + publication volume by year.

- **Ratings & Sentiment Profile:**  
  Overall rating distribution (1–5) and positivity skew.

- **Popularity vs. Quality (Books):**  
  Ratings count and average rating per title to identify high-engagement books.

- **Author Performance (Volume-Aware):**  
  Top authors by average rating with adaptive minimum rating thresholds for robustness.

- **Publisher Performance (Quality vs. Volume):**  
  Publishers with ≥5 substantial titles (>50 pages), ranked by average rating.

- **Reader Engagement Behaviour:**  
  Review activity among highly engaged raters (users who rated >50 books).

---

## <img src="icons/dataset.png" width="30">  &nbsp;&nbsp;Dataset

**Tables used**
- `books` — `book_id`, `author_id`, `title`, `num_pages`, `publication_date`, `publisher_id`  
- `authors` — `author_id`, `author`  
- `publishers` — `publisher_id`, `publisher`  
- `ratings` — `rating_id`, `book_id`, `username`, `rating`  
- `reviews` — `review_id`, `book_id`, `username`, `text`

⚠️ **Reproducibility note**  
The original version ran on PostgreSQL during the bootcamp.  
This repository includes **CSV snapshots** in `data/samples/` and recreates the schema using an **in-memory SQLite** engine,  
so all queries can be executed locally via `pd.read_sql()`.

---

## <img src="icons/conclusions.png" width="30">  &nbsp;&nbsp;Key Insights

- **Contemporary catalogue:**  
  **819 books (~82%)** were published after **January 1, 2000**, with publication volume increasing notably post-2000.

- **Positive reader sentiment:**  
  Ratings concentrate around **4–5**, suggesting generally favourable user sentiment.

- **Authors combine engagement and quality:**  
  High-volume authors such as **J.K. Rowling/Mary GrandPré (~4.29)** and **J.R.R. Tolkien (~4.24)** show consistently strong reception,  
  while **Stephenie Meyer (~3.66)** has high engagement but more polarised ratings.

- **Publishers show stable quality:**  
  Among publishers with **≥5 books >50 pages**, average ratings cluster tightly (**~4.13–4.45**).  
  Top performers include **Harper Voyager (4.45)**, **Vertigo (4.37)**, **HarperCollins Publishers (4.32)**,  
  **Harper Perennial Modern Classics (4.31)** and **Random House (4.25)**.

- **Publisher volume leader:**  
  **Penguin Books** released the highest number of substantial titles (>50 pages).

- **Highly engaged users are valuable contributors:**  
  Users who rated **>50 books** write an average of **~24 reviews**, representing a segment that can be activated to strengthen community content.

---

## <img src="icons/impact.png" width="30">  &nbsp;&nbsp;Product & Business Impact

- Provides a decision-ready view of **catalogue recency** and **platform sentiment**.
- Identifies authors and publishers suitable for **recommendation boosts** and **editorial curation**.
- Highlights a high-engagement cohort to support **community and retention strategies**.
- Demonstrates SQL-driven reporting with a portable setup suitable for stakeholder review.

---

## <img src="icons/recommendations.png" width="30">  &nbsp;&nbsp;Recommendations

- **Personalised discovery:** prioritise recommendations using a combined signal of rating volume + average rating.
- **Editorial highlights:** feature high-performing publishers/authors in curated collections and themed campaigns.
- **Review activation:** prompt highly engaged raters (>50 ratings) to write more reviews (badges, prompts, visibility boosts).
- **Experimentation:** A/B test small ranking boosts for high-quality catalogues and measure downstream engagement.
- **Next iteration:** add genre/topic labels and lightweight review sentiment analysis to improve recommendation relevance.

---

## <img src="icons/techstack.png" width="30">  &nbsp;&nbsp;Tech Stack

- **Languages & Tools:** Python, SQL  
- **Database:** SQLite (in-memory)  
- **Analysis & Queries:** SQL via `pd.read_sql()`  
- **Environment:** Jupyter Notebook  
- **Visualisation:** Matplotlib  
- **Data Handling:** CSV snapshots (`data/samples/`) for portability  
- **Version Control:** Git & GitHub  

---

<p align="center">
  <sub>📊 Designed & developed by <b>Marcela Maris</b> — Data Analytics Portfolio</sub><br>
  <sub><i>SQL Analytics • Business Reporting • Product Insights</i></sub>
</p>


