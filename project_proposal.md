# Project Proposal

The purpose of this project is to retrieve the data from boxofficemojo.com using web scraping technique, analyze it, and understand what factors affect the revenue of a movie and how do they affect it.

### The main questions of this project will be:

1. What factors affect the movie revenue?
2. How these factors affect it? (How does the change in one factor(feature) changes the revenue(target)?)

### Data description

The main dataset for this project will be data scrapted from boxofficemojo.com website. The main features of the data will be: budget of the movie, genre, rating, actors, release year, studio that created it
There are additional datasets may be used during analysis, such as the data from imdb.com

### Tools used

The analysis will be done using python. Data will be scraped from websites using beautiful soup module, then pandas will be used for data analysis and data manipupation. sklearn module will be used to build a linear regression model, and Matplotlib and Seaborn - for data visualization.

### MVP

The MVP for this project would be a linear regression model representing one or two features and their affect on our target(movie revenue)