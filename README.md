# movie-industry-eda

# Purpose
Do an Exploritory Data Analysis of the movie industry to answer the question, "What types of films are currently doing the best at the box office?" and provide some actionable insights from that analysis.

# Summary of Results

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
