# End-to-End BI Pipeline for IMDb Movie & Series Insights


## 📌 Project Summary  
This end-to-end BI project explores the massive **IMDb open dataset** (100M+ records) and demonstrates my ability to:  

✅ Design scalable ETL pipelines  
✅ Normalize and model complex, nested data  
✅ Build a dimensional data warehouse in **Snowflake**  
✅ Create insights via interactive **Tableau dashboards**  

---

## 🧠 Business Requirements Solved  
As a **Business Analyst**, this solution allows users to:  
- 🎭 Find all professions (actors, producers, writers) for a person  
- 🎞️ List movies by genre, region, adult flag, and year  
- 📊 Track movie lengths and rating trends over time  
- 🧑‍🤝‍🧑 Analyze cast, crew, jobs, and characters by title  
- 🌍 Explore multi-language/movie title variations across countries  
- 📈 Identify top-rated films per year and genre  
- 📺 Compare series seasons, episode counts, and ratings  

---

## 🗂️ Datasets Used  
| File                     | Description                                | Records     |
|--------------------------|--------------------------------------------|-------------|
| `name.basics.tsv`        | Actor, Director, Crew Info                 | 14M+        |
| `title.basics.tsv`       | Movie/Show Metadata                        | 11.4M       |
| `title.akas.tsv`         | Alternate Titles, Regions, Languages       | 51M+        |
| `title.crew.tsv`         | Directors & Writers                        | 11.4M       |
| `title.episode.tsv`      | TV Episodes, Seasons, Series Linkage       | 8.8M        |
| `title.principals.tsv`   | Principal Cast & Crew per Title            | 90M+        |
| `title.ratings.tsv`      | Ratings & Vote Count                       | 1.5M        |

---

## 🛠️ Tech Stack  
| Category         | Tools Used                                                                 |
|------------------|----------------------------------------------------------------------------|
| Data Profiling   | `Alteryx`, `Python`, `YData Profiler`                                     |
| ETL Pipelines    | `Azure Data Factory`, `SQL`, `Alteryx`                                    |
| Data Warehouse   | `Snowflake` (Medallion Architecture)                                      |
| Data Modeling    | `ER Studio` (Dimensional Star Schema)                                     |
| Visualization    | `Tableau` – Dashboards (Trends & Genre Insights)                        |

---

## 🧼 Data Engineering Process  

### 🧱 Medallion Architecture  
**Bronze → Silver → Gold** implemented using Snowflake & ADF:  
- **Bronze**: Raw ingestion (IMDb TSV to Snowflake)  
- **Silver**: Cleaned, flattened, normalized in Alteryx  
- **Gold**: Star schema: fact & dimension tables for BI  

---

### 🔄 Cleaning & Transformation Highlights  
- Replaced all `\N` (nulls) with `"Unknown"` or `0` for consistency  
- Split arrays (e.g., genres, known titles, crew IDs) using `Text to Columns`  
- Trimmed white spaces, fixed types (`ratings` as float)  
- Mapped ISO Country & Language codes for localization insights  
- Created normalized genre and job/character tables for easier joins  

---

## 🧾 Star Schema Design  
✅ One row per rating, episode, cast/crew-role, genre-tag  
- `DIM_TITLE`, `DIM_GENRE`, `DIM_PERSON`, `DIM_REGION`, `DIM_LANGUAGE`  
- `FACT_RATING`, `FACT_EPISODE`, `FACT_JOB`, `FACT_CHARACTER`  

---

## 📊 Tableau Dashboards  

### 📅 Dashboard 1: Movie Trends  
- Movie Releases Over Years  
- IsAdult vs. Non-Adult Trends  
- Country-wise Movie Counts  
- Ratings Distribution

![Dashboard_P1_MovieTrendsAndReleases](https://github.com/user-attachments/assets/83e9400f-4f64-4136-a217-f12e472ab7b0)

### 🎭 Dashboard 2: Genre & People Analysis  
- Most Frequent Genres  
- Role-based Contribution Breakdown (Actor, Director, etc.)  
- Profession & Job Role Distribution  

![Dashboard_P2_AgeWiseDataTrends](https://github.com/user-attachments/assets/7ec86fb6-526b-4587-a6be-f6e00703e370)

---

## 💡 Key Skills Demonstrated  

| Area                 | Examples Shown                                                                 |
|----------------------|--------------------------------------------------------------------------------|
| Data Engineering     | Cloud DW setup, schema creation, Snowflake privileges, data normalization     |
| Data Analysis        | Parsing complex relationships (e.g., crew-title links), genre trend analysis  |
| Business Intelligence| Use-case driven dashboards for stakeholders                                   |
| ETL Automation       | ADF pipeline creation for fact/dimension loads                                |

---

## 📈 What This Project Proves  
- Mastery of **cloud-based warehousing and ETL pipelines**  
- Confidence working with **large-scale, nested, and multilingual data**  
- End-to-end ownership from **data ingestion to insights delivery**

## Dimensional Model

![Dimensional_Model](https://github.com/user-attachments/assets/fc7f9737-c2a7-4d58-b08e-95777d39295f)

## Pipeline (Azure Data Factory)

![Pipeline](https://github.com/user-attachments/assets/2af68739-f7fd-4c4e-a9f1-e5c971e07a62)

---

**Feel free to fork, explore, and contribute!**
📬 Let’s connect on [LinkedIn](https://www.linkedin.com/in/je-pulipati/) If you’re hiring for Data Engineering, Analytics, or BI intern roles im open hiring!

---
