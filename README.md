# 🎬 Movie Database SQL Exploration

This project explores a movie database using **SQL** to answer a series of real-world queries related to movies, actors, genres, awards, and production data. The goal is answer questions related to SQL database by filtering, aggregation, joins, string manipulation, and subqueries.

The SQLite Database used for this purpose is loaded together with the project file

---

## 📂 Project Structure

- SQL queries are written using standard SQL (compatible with MySQL).
- Each query answers a specific business or data-driven question using the movie database.
- The dataset contains tables like `movies`, `oscars`, `actors`, `genres`, `production_companies`, and `keywords`.

---

## ✅ Questions Answered

1. **🏆 Who won the Oscar for “Actor in a Leading Role” in 2015?**
2. **🎥 What query will produce the ten oldest movies in the database?**
3. **🏅 How many unique awards are there in the Oscars table?**
4. **🕷️ How many movies are there that contain the word “Spider” within their title?**
5. **💘 How many movies are there that are both in the "Thriller" genre and contain the word “love” in their keywords?**
6. **📅 How many movies were released between `2006-08-01` and `2009-10-01` with a popularity score > 40 and budget < 50 million?**
7. **🎭 How many unique characters has *Vin Diesel* played in the database?**
8. **🎬 What are the genres of the movie “The Royal Tenenbaums”?**
9. **🏢 What are the top 3 production companies with the highest average movie popularity score?**
10. **👩‍🎤 How many female actors (gender = 1) have names starting with the letter "N"?**
11. **📉 Which genre has, on average, the lowest movie popularity score?**
12. **🎓 Which award category has the highest number of actor nominations?**

---

## 🛠 Technologies Used

- **SQL** for querying
- **Movie database** (SQLite)
- **GitHub** for version control and project sharing

---

## 🚀 Getting Started

To run or replicate these queries:

1. Import the movie database into your SQL environment (e.g., PostgreSQL, MySQL).
2. Open your SQL editor and run the queries available in this repository.
3. Ensure your database schema aligns with assumed table structures: `movies`, `oscars`, `genres`, `actors`, `keywords`, `production_companies`.

---

## 📌 Highlights & Learnings

- Practiced real-world SQL filtering and pattern matching with `LIKE`, `ILIKE`.
- Used `JOIN`, `GROUP BY`, and `HAVING` to solve aggregation problems.
- Explored subqueries and ordering for top results and rankings.
- Analyzed actor roles, gender-based queries, and genre-based analytics.


---
## Sample query
``` sql
%%sql
-- 1. Who won the Oscar for “Actor in a Leading Role” in 2015?
SELECT * 
FROM oscars
WHERE winner = 1.0
and
      year = 2015   
and 
    award = "Actor in a Leading Role"
limit 5

