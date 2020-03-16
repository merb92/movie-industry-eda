# movie-industry-eda

# Purpose
Do an Exploritory Data Analysis of the movie industry to answer the question, "What types of films are currently doing the best at the box office?" and provide some actionable insights from that analysis.

# Summary of Results

I based my analysis around what types of movies to choose in order to have the best return on investment and probability of profitability.

Return on investment would be finding the movie types that would provide the highest profits.

Probability of Profitability would be finding what movie types would provide the highest probability of making at least $0.01.

The commercial movie industry has been around since the late 19th century, but the entertainment habits and tastes for current movie watchers are what I was interested in, so I limited the movie data to movies made in the year 2000 up to mid 2019 (the most recent data available).

I started by adjusting all the historical monetary values for inflation, so that there was a standard buying power per dollar across the dataset.

The first question I wanted to answer was, "If we built it, will they come?". Meaning, are movies profitable by default, and is profit correlated to the production budget.

In the first case, I found that no, movies are not profitable by default; in fact, 32% of the movies in the dataset made zero profit or lost money?

Looking at the correlation between profit and production budget is a more complicated story. When looking at all the data in the dataset, the correlation is 0.63, which is a solid moderate correlation, but when looking at the visualization of profit vs. production budget, it doesn't look like the data has that much of a correlation. When looking at the bulk of the dataset it looks like a rectangle. I then split up the data into 10 quantiles to check the correlation in each. I found that there was essentially no correlation between the two variables until the 10th quantile, where it had a correlation of 0.45. Therefore it is only for the movies with the very highest production budgets that there is even a moderate correlation between the two.

Next, I looked at the probability of profit for each quantile of production budget. I found that there is a positive linear relationship between the amount of money spent on the production budget of a movie and the probability of profit. It starts at 53% for the 1st quantile and goes up to 90% for the 10th quantile.

From the standpoint of running a movie studio it is reassuring to know that the more money that is spent on production the less likely the movie will lose money, but it isn't on its own enough information to run a for profit studio. That studio will also want to know what types of movies to make to have a good return on the investment in the movies it produces.

I next looked at what genres of movies are the most profitable.

First, I looked at the percentage of movies per genre that are profitable and found that Animation had the highest percentage of movies that were profitable.

I next wanted to know about the profitability of each genre and how that relates to the percentage that are profitable.

It turns out here that in most cases Animation is the most profitable. It has the highest average profit per movie. Given the amount of extreme outliers in our dataset, median was used to illustrate the average.

I then looked at the 3rd Quantile of profit per genre, followed by the upper whisker of profit for genre and in both cases Animation was on top.

It was only when I looked at the maximum profit per genre, did other genres show more profit than Animation. Those genres were: Adventure, Fantasy, Sci-Fi, Action, Thriller, and Crime.

In these genres there were 37 movies that were more profitable than the upper whisker of profit in the Animation genre, and the first noticeable attribute of them was that so many were part of movie franchises. After researching each movie, I found that 81% of them were part of a movie franchise.

From the analysis done so far I have the following recommendations.

Focus on the Animation genre, it is the the most likely to be profitable and that profit will likely be higher than the other genres.

Keep an eye out for Action/Adventure/Fantasy/Sci-Fi movies that have franchise potential because they have the potential to make the highest profits although there is more financial risk involved.

Future Work

Further analyze movies in the Animation genre to find other attributes that would help increase the probability of profit and return on investment

Further analyze the movies in the Action/Adventure/Fantasy/Sci-Fi genres to find out what could help give the movie extreme profits besides the movie being part of a franchise.

Analyze how the production budget could be split up according the attributes found in the two above suggestions for future work.

Include an analysis of the marketing side of the movie industry.

# Requirements
Python 3.6+

The following Python libraries:
* pandas
* seaborn
* matplotlib
* cpi
* requests
* json
* math
* warnings
* time
* ast
* numpy

API access to www.themoviedb.org 

Instructions on getting API access can be found at https://developers.themoviedb.org/3/getting-started/introduction 

Jupyter Notebook server version 5.7.8+

# Datasets
* Datasets provided for the project, originally found at https://github.com/learn-co-students/dsc-mod-1-project-v2-1-onl01-dtsc-pt-012120, copies of which are stored in the datasets directory.  This includes data from Box Office Mojo, IMDB, Rotton Tomatoes, The Movie Database and The Numbers.
* Data queried from www.themoviedb.org using their API

# Usage
* Download repo
* Open index.ipynb in Jupyter notebook
* Run All
* Please note,the API queries are in the TMDB_Genres.ipynb and Get_Missing_Genres_TMDB.ipynb files.  Since those API queries have already been run and the results saved in .csv files in the datasets directory, they do not need to be rerun in order to run index.ipynb.  Get_Missing_Genres_TMDB.ipynb files has some hardcoded data cleaning of strings, if the underlining data changes, this datacleaning may fail and need updated.
