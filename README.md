# 🎬 Netflix Movies & TV Shows Data Analysis using PostgreSQL

## 📌 Project Overview

This project focuses on performing end-to-end data analysis on the Netflix Movies and TV Shows dataset using PostgreSQL.

The main objective of this project is to solve real-world business problems using SQL and extract meaningful insights from raw data.

This project demonstrates:
- Data Cleaning
- Data Exploration
- Business Insight Generation
- Advanced SQL Querying
- Window Functions
- String Manipulation
- Aggregations & Filtering

---

# 🛠️ Tools & Technologies Used

- PostgreSQL
- pgAdmin 4
- SQL
- Kaggle Dataset

---

# 📂 Dataset Information

### Source
Netflix Movies and TV Shows Dataset from Kaggle

### Total Records
8,807 rows

### Main Columns
- show_id
- type
- title
- director
- casts
- country
- date_added
- release_year
- rating
- duration
- listed_in
- description

---

# 🗄️ Database Setup

## Create Table

```sql
CREATE TABLE netflix(
	show_id VARCHAR(10),
	type VARCHAR(10),
	title VARCHAR(200),
	director VARCHAR(300),
	casts VARCHAR(1000),
	country VARCHAR(200),
	date_added VARCHAR(50),
	release_year INT,
	rating VARCHAR(20),
	duration VARCHAR(50),
	listed_in VARCHAR(200),
	description VARCHAR(400)
);
📥 Data Import

The dataset CSV file was imported into PostgreSQL using the pgAdmin Import/Export feature with:

Header enabled
Correct delimiter configuration
Proper column mapping
📊 Business Problems Solved
1️⃣ Count Movies vs TV Shows

Analyzed the distribution of Movies and TV Shows available on Netflix.

Skills Used
GROUP BY
COUNT()
2️⃣ Most Common Rating

Identified the most common content rating for Movies and TV Shows.

Skills Used
Window Functions
RANK()
PARTITION BY
3️⃣ Movies Released in 2020

Filtered all movies released in the year 2020.

Skills Used
WHERE
Filtering
4️⃣ Top 5 Countries with Most Content

Extracted the top countries producing Netflix content.

Skills Used
STRING_TO_ARRAY()
UNNEST()
Aggregation
5️⃣ Longest Movie

Found the movie with the longest duration.

Skills Used
SUBSTRING()
POSITION()
Type Casting
6️⃣ Content Added in Last 5 Years

Retrieved recently added content using INTERVAL.

Skills Used
TO_DATE()
CURRENT_DATE
INTERVAL
7️⃣ Director Specific Analysis

Found all content directed by Rajiv Chilaka.

Skills Used
ILIKE
Pattern Matching
8️⃣ TV Shows with More Than 5 Seasons

Identified long-running TV shows.

Skills Used
SPLIT_PART()
9️⃣ Genre-wise Content Count

Calculated total content items for each genre.

Skills Used
STRING_TO_ARRAY()
UNNEST()
GROUP BY
🔟 India Content Release Analysis

Calculated yearly Netflix content release trends for India.

Skills Used
EXTRACT()
Aggregation
1️⃣1️⃣ Documentary Movies

Filtered all documentary-related content.

Skills Used
LIKE
String Filtering
1️⃣2️⃣ Missing Director Analysis

Identified content without director information.

Skills Used
NULL Handling
1️⃣3️⃣ Salman Khan Movies Analysis

Tracked Salman Khan movies released in the last 10 years.

Skills Used
EXTRACT()
CURRENT_DATE
ILIKE
1️⃣4️⃣ Top 10 Actors in Indian Movies

Identified actors appearing most frequently in Indian movies.

Skills Used
UNNEST()
STRING_TO_ARRAY()
Aggregation
1️⃣5️⃣ Content Categorization

Categorized content into:

Good_Content
Bad_Content

based on keywords like:

kill
violence
Skills Used
CASE WHEN
CTEs
Pattern Matching
🚀 Advanced SQL Concepts Used
Common Table Expressions (CTEs)
Window Functions
RANK()
PARTITION BY
String Functions
Date Functions
INTERVAL
Type Casting
Aggregations
Pattern Matching
NULL Handling
📈 Key Insights
Movies dominate Netflix content compared to TV Shows.
Certain countries contribute significantly more content.
Drama and International genres are highly popular.
Long-running TV shows have strong platform presence.
Many content descriptions contain violence-related keywords.
India is among the major contributors to Netflix content.
