# Investigate-the-TMDb-Movies-Database

### Description
This is one of the final project of my Data Analyst ND on Udacity. The project involved analyzing a provided dataset for insights using the the necessary Python libraries, reporting findings and limitations of each analysis.

I picked the TMDb Movies dataset (movies.csv) and carried out answering the following questions:

- Which Director collected more year best selling movie?
- Has the year average movie budget increased or decreased for most recent movies?
- Does the increase/decrease translate in more profitable movies?
- How popularity and profitable movies are related?
- Does a bigger budget result in a higher popularity score?
- Which genre was the most represented over the years? Can we see any changes between old and recent movies?

### Libraries

- Pandas
- Numpy
- Matplotlib
- Seaborn
- Statsmodels

### Wrangling and Cleaning

Dataset shape: (10866, 21)

I have dropped some of the columns not useful for the analysis sonce they are redundant or don't add any value.
Importantly, both "vote_count" and "vote_average" columns(respectively the number of votes and the mean grade for each movie) needed to be dropped due to inconsistencies of the values combined with lack of knowledge of the voting process.

In terms of duplicates, I have dropped the only occurrence of an entire row duplicated.

There are some NULL values in the remaining dataset, however they didn't have any impact on the analysis so I kept them.

On the other hand, there are five occurrences of a ZERO in either the "budget_adj" or "revenue_adj" column which are meaningless. I therefore dropped those rows.

### Conclusions
The most successful director in terms of number of year best selling movies is Steven Spielberg.

Despite an increase in the yearly average movie budget in most recent years, the yearly average profit decreased. However, a positive, though weak, correlation between movie budget and profit exists.

A stronger positive correlation has been found instead between popular movie and profit, although unclear how the popularity metric has been calculated. This may identify the popularity metric as a good predictor for a profitable movie. Additionally, the weakness of the positive correlation between budget and popularity shows that not always spending more lead to popular and profitable movies.

Lastly, the four most rapresented genres were always the same for every period analysed. Interestingly enough, the only change over the years involved thrillers which surpassed action movies as third most rapresented genre in recent period. Conversly the lead of drama movies, followed by comedies kept steady in first and second place resperctively across all periods.
