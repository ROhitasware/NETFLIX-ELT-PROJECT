## **📽 Netflix ELT Data Pipeline Project

### **🧰 Tech Stack:**

* **Languages & Tools:** Python, SQL
* **Libraries:** Pandas, Matplotlib, Seaborn

---

### **📌 Project Overview:**

This project aimed to simulate an end-to-end **ELT (Extract, Load, Transform)** data pipeline to derive meaningful insights from Netflix's content data. Netflix, as a leading OTT platform, generates vast amounts of content-related data, which can be analyzed to understand trends, preferences, and global content distribution.

The project was carried out in **three major phases:**

1. **Extract:**

   * Collected Netflix dataset from a publicly available source (e.g., Kaggle).
   * Loaded raw CSV data into a working environment using Pandas.
   * Handled missing data, inconsistent data types, and categorical values.

2. **Load:**

   * Designed relational database schema using PostgreSQL to represent shows, genres, country, and cast members.
   * Inserted cleaned and structured data into PostgreSQL tables using Python's `psycopg2` or `sqlalchemy`.
   * Ensured data type consistency, added primary-foreign key constraints, and normalized the database.

3. **Transform:**

   * Wrote SQL queries to perform complex data transformations (e.g., extracting year from date\_added, parsing multiple genres/countries).
   * Created views and temporary tables to aggregate and analyze data (e.g., content count per year, per country, genre popularity, etc.).
   * Joined tables to produce comprehensive datasets ready for reporting and dashboarding.

---

### **📊 Detailed Data Analysis and Insights:**

1. **Content Growth Over Time:**

   * Analyzed yearly trends of newly added titles.
   * Observed a rapid rise in content post-2016, reflecting Netflix's global expansion.

2. **Top Producing Countries:**

   * Identified countries with the most content production (e.g., USA, India, UK).
   * Detected regional variations in content types (e.g., drama, comedy, documentary).

3. **Genre-Based Insights:**

   * Parsed multi-genre fields and normalized them for analysis.
   * Determined most common genres across regions and time.
   * Found Drama and International Movies to be dominant in Netflix’s catalog.

4. **Content Type Distribution:**

   * Compared Movies vs TV Shows in the platform’s offerings.
   * Movies formed \~70% of content, with TV shows increasing steadily over time.

5. **Director & Cast Analysis:**

   * Cleaned and tokenized cast/director data to build a frequency distribution.
   * Identified top contributors by number of appearances or directed content.

---

### **🗂 Data Modeling and Schema Design:**

* **Tables Created:**

  * `titles (title_id, title_name, type, description, release_year, date_added, duration)`
  * `genres (genre_id, genre_name)`
  * `title_genres (title_id, genre_id)`
  * `countries (country_id, country_name)`
  * `title_countries (title_id, country_id)`
  * `cast_members (cast_id, cast_name)`
  * `title_cast (title_id, cast_id)`
  * `directors (director_id, director_name)`
  * `title_directors (title_id, director_id)`

* Normalized data to reduce redundancy and improve query performance.

* Ensured data consistency with foreign key constraints and indexes.

---

### **📈 Visualizations and Reporting:**

Although the core of this project focused on building the ELT pipeline, visualizations were included for presentation and storytelling:

* **Bar Charts**: Year-wise title additions, genre counts.
* **Pie Charts**: Movies vs TV Show share, genre distribution.
* **Heatmaps**: Content production density across countries.
* **Line Graphs**: Growth trends in title addition over time.

Visuals were generated using **Matplotlib** and **Seaborn**, embedded in the final notebook.

---

### **🧠 Key Learnings and Takeaways:**

* Gained hands-on experience building a robust **ELT pipeline** from scratch.
* Understood schema design, **data normalization**, and **relational modeling** for real-world datasets.
* Practiced writing complex SQL queries for data transformation and aggregation.
* Learned how to prepare **analytically ready datasets** suitable for dashboarding and BI tools.
* Recognized the importance of **data cleaning, deduplication, and parsing** multi-value fields like genre and cast.

---

### **📦 Optional Enhancements:**

* **Airflow** could be introduced to automate the ELT process using DAGs.
* **dbt** can be integrated for transformation logic version control and modular SQL.
* Connect the cleaned dataset to **Power BI** or **Tableau** for advanced dashboards.
* Implement a REST API using Flask to expose endpoints for querying titles by genre/year.

---

### ✅ Final Outcome:

The completed Netflix ELT project showcases the practical application of data engineering and analytics skills, transforming raw and messy data into structured, insightful content. It demonstrates your ability to:

* Build data pipelines
* Manage relational databases
* Perform real-world data transformation
* Deliver value through analytical storytelling

---


