# Phase 1 Project

## Project Description:
I am collecting and cleaning data from credible websites with data on movie grossings, budgets, ratings, release dates, ext. to help Microsoft determine conditional factors that could help determine a successful movie to invest in. I am going to use data analysis to help Microsoft determine several conditions that may be condusive to producing a film with high returns.

### 1.1 Data:

In the folder `zippedData` are movie datasets from:

* Box Office Mojo
* IMDB
* Rotten Tomatoes
* TheMovieDB.org

Specific folders inclue:
zippedData/imdb.name.basics.csv.gz
zippedData/imdb.title.ratings.csv.gz
zippedData/imdb.title.basics.csv.gz
zippedData/bom.movie_gross.csv.gz
zippedData/tn.movie_budgets.csv.gz




#### 1.1.1 Data Cleaning

For this project I ended up mostly using about 4 data sets, most of which came from IMDB.  The data sets combined were over 5000 entries and had a lot of NaN values to start.  I began by joining all of the tables into one large table, dropping all of the NaN values, and dropping duplicates.  This helped bring it down to about 2500 entries.  The main concern was that some of the value columns were strings with dollar signs and commmas so all of those columns had to be converted to integers and be stripped of any symbol that wasn't a number.  I also attempted to remove any outliers from the data by calling the the stats package and using the z-score to remove anything that had a z-score less than 3.

### 1.2 Key Findings:

#### 1.2.1 Do ratings have any affect on the amount a movie grosses?

Here I used the zippedData/imdb.title.ratings.csv.gz and the zippedData/bom.movie_gross.csv.gz data sets to find out if there was a relationship between having a high rating and a film making a large worldwide gross.  Tables had to be joined and cleaned by dropping rows with missing values, changing data types, and removing extra symbols like commas and dollar signs.


![image_one]fig1.png

![](fig1.png)

Key Findings:
1. Ratings have essentially no impact on the financial success of a film.
2. However budget does have some sort of effect on revenue. You do not necessarily need the highest budget, but a budget of at least 100 million will more than likely impact the success of a film positively.   
    
Recommendations:
Do not worry about the critical reception of a film, instead focus and budgeting out for the resources and labor to make a good film.
    

#### 1.2.2 What time of year is the best time of year to release a film?

For this I used zippedData/tn.movie_budgets.csv.gz data file.  It needed cleaning mostly by making separate columns that contained the release month by abbreviation and by numerical month of the year.  This helped me to organized the data by month and compare it to the worldwide gross.

Key Findings:

1. The best times of year to release a film are June, July, and August, as well as November, December, and January.  
2. Findings seem accurate because these times of the year are synonmys with staying indoors due to extreme heat or cold as well as holidays.  

Recommendations: 
Plan to start filming and editing so that it will be ready for either the summer or winter.  

#### 1.2.3 Should you push to a worldwide market?

For this I used the movie_budgets_df.head() data file.  It needed some cleaning to strip the numbers of any dollar signs or commas and get rid of any missing values.  I layerd two bar plots on top of eachother to get a visual representation of how much the non domestic gross makes up of the total gross.  I also categorized them by genre so we could see what genres make the most revenue as well as how much of the revenue was not domestic.

Key Findings:

1. The movie genres with the highest revenues was Action, Adventure, Animation, and Mystery.
2. A substantial portion of the revenue was from worldwide gross in almost every category.  It accounted for more than 50% of the revenue in most of the high grossing genres. 


Recommendations:  Make an Action/Adventure/Mystry film that is targeted to a worldwide audience.

### 1.3 Conclusion:

After working with this data, I think it would be best to make a film that is Action, Adventure, Animation, or Mystery that is going to be released during the Summer or Winter holidays.  Make sure that the film is being marketed towards an international market.  Budget was one of the biggest discoveries of this research.  The biggest finding is that yes, budget does have an impact on revenue.  However, the largest budget does not yield the highest rating.  From my findings I feel like a budget of 100-250 million is the spot where most films had high revenue, but anything over that did not necissarily ensure higher ratings.


### 1.4 What Next?

Some of the questions to ask ourselves as we look at moving forward with this project based on our findings. 

What is the exact range for creating a budget?  Can we narrow down what the budget should be within a few hundred thousand?  
Does genre of movie correlate with time of year?
Worldwide market trends by genre.
Looking into specific Actors, Directors, ext. of each genre.


```python

```
