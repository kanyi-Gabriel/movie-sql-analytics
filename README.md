#  Movie Database SQL Exploration

This project explores a movie database using **SQL** to answer a series of real-world queries related to movies, actors, genres, awards, and production data. The goal is answer questions related to SQL database by filtering, aggregation, joins, string manipulation, and subqueries.

The SQLite Database used for this purpose is loaded together with the project file


## Getting Started (Requirements to run the project on Jupyter Notebook)

##### Beginner-Friendly MySQL Setup in Jupyter Notebook
This guide helps you set up a connection to a local MySQL database using Jupyter Notebook. You’ll be able to test the connection and confirm everything is working by viewing a table.


#####  Step 1: Install Required Packages

**Run this code block in a Jupyter Notebook cell:**

       !pip install ipython-sql==0.4.1
       !pip install pymysql
       !pip install mysql-connector-python
       !pip install cryptography
       !pip install prettytable==0.7.2
       !pip install SQLAlchemy==1.4.49

 Once the installation is done, it's a good idea to restart the kernel before continuing. This ensures all packages load properly.


## Questions Answered

1. **Who won the Oscar for “Actor in a Leading Role” in 2015?**
2. **What query will produce the ten oldest movies in the database?**
3. **How many unique awards are there in the Oscars table?**
4. **How many movies are there that contain the word “Spider” within their title?**
5. **How many movies are there that are both in the "Thriller" genre and contain the word “love” in their keywords?**
6. **How many movies were released between `2006-08-01` and `2009-10-01` with a popularity score > 40 and budget < 50 million?**
7. **How many unique characters has *Vin Diesel* played in the database?**
8. **What are the genres of the movie “The Royal Tenenbaums”?**
9. **What are the top 3 production companies with the highest average movie popularity score?**
10. **How many female actors (gender = 1) have names starting with the letter "N"?**
11. **Which genre has, on average, the lowest movie popularity score?**
12. **Which award category has the highest number of actor nominations?**



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

