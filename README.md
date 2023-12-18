# Microsoft Movie Studio Project
![Image from web](https://tibs.ac.ke/uploads/course_cover_images/FILM_PRODUCTION_1.jpg)


**Author :** Kennedy Owino


## Business Problem


Microsoft sees all the big companies creating original video content and they want to get in on the fun. They have decided to create a new movie studio, but they don’t know anything about creating movies. You are charged with exploring what types of films are currently doing the best at the box office. You must then translate those findings into actionable insights that the head of Microsoft's new movie studio can use to help decide what type of films to create.

## Business Understanding

In order to guide the decision-making process for Microsoft's new movie studio, it is imperative to conduct a comprehensive analysis of the current trends and successes in the film industry. One key aspect involves examining the types of films that have been performing exceptionally well at the box office. This entails studying recent blockbuster releases, assessing their genres, themes, and audience demographics, and identifying patterns that correlate with high financial returns. Additionally, it is essential to delve into the evolving preferences of global audiences, considering factors such as cultural diversity, emerging storytelling techniques, and the impact of digital platforms on viewership patterns.

Furthermore, a thorough examination of the competitive landscape is crucial to position Microsoft's movie studio strategically. This involves evaluating the strategies employed by other major players in the entertainment industry who have successfully ventured into original content creation. Analyzing the marketing and distribution approaches, as well as the critical and audience reception of recent blockbuster films from rival studios, will provide valuable insights into the dynamics of the market. The goal of this project is to distill these findings into actionable insights that will enable Microsoft's movie studio to make informed decisions about the type of films to produce, ensuring alignment with current market trends, audience preferences, and industry competition.


### Objectives of the Project


$i).$ Identify the types of films currently performing well at the box office
<br>
$ii).$ Identify genres with the highest production budget
<br>
$iii).$ Analyse trends in audience preferences and genres.
<br>
$iv).$ Estimate the best time to release a profitable movie.



## Data Understanding

The data utilized for this project was obtained from learn-co-curriculum Git repository.
<br>
The datasets include information from Box Office Mojo, IMDB, Rotten Tomatoes and TheMovieDB.org
<br>
This data included: movie titles, premiere dates, box office gross (domestic & foreign), ratings, reviews, and movie synopses. The data gives a overview of all theatre released movies up until 2019.

<br>
For this project  `tn.movie_budgets.csv.gz` was utilized  and extracted `movie_basic`and `movie_ratings` tables from `id.db` database.


## Data Preparation

Import the `tn.movie_budgets.csv.gz` as `movie_budgets`. Remove '$' signs in the `production_budget`, `'domestic_gross'`, `'worldwide_gross'` columns using the `.split()` method then conver the columns from 'object' type to 'float'. There were no missing values in this dataset.

Then I moved on to query the `movie_basics` and `movie_rating` tables from `id.db` database and store the results in variable called `movie_basics`. 
There were movies with missing genres and for this case, i created a new category, `non_defined` genre to represent movies with missing genres.

For movies with multiple genres I split the genres to component genres to the `.explode` the list of genres to create new separate records.

$.$ `movie_basics` and `movie_budget` dataframes were merged to  create a new dataframe to be used for the analysis.


## Exploratory Data Analysis

$-$ From the plots, Drama, Comedy and Action genres emrged as the most common genres in the movie industry

$-$ Animation, Adventure and Sci-Fi emerged as the leading genres boasting the highest production budgets, reflecting substantial investments in these categories. Conversely, genres such as Music, News, and Horror occupy the lower spectrum of production budgets, signifying more conservative financial allocations for movies within these genres.

$-$ Animation, Adventure, and Sci-Fi stand out with the highest domestic and worldwide gross figures. In contrast, genres like News, War, and Documentary appear to have the lowest worldwide and domestic gross, indicating comparatively lower financial performance in terms of box office revenue for movies within these genres.

$-$ The majority of movies have a runtime averaging around 94.65 minutes. Additionally, the correlation coefficient of 0.214 between runtime and profit suggests there is limited evidence supporting the notion that an extended runtime significantly contributes to higher profit margins.

$-$ A correlation of 0.215 between movie ratings and profit implies that there is only a modest relationship between the two variables. This finding suggests that a movie's rating has limited influence on its profit margins. While viewer ratings can impact a movie's reception, other factors likely play a more substantial role in determining its financial success.

$-$ Movies released between April and July exhibited higher average profit margins compared to those released during other months of the year. This temporal trend suggests that there may be favorable conditions or market dynamics during this period that contribute to increased profitability for movies.


## Recommendations

There are may other factors that we might come to play while considering production of a succesful and profitable movie, such as role played by directors, actors et al. From EDA performed in this project recommend the following:

$1.$ Microsoft stands to gain substantial returns on investment by strategically entering the Animation, Sci-Fi, and Adventure genres. These genres have consistently proven to be the most popular, demonstrating a robust track record of higher profitability in the film industry.

$2.$ For optimal financial performance, it is advisable for Microsoft's movie studio to target a runtime range of 90 to 110 minutes. This recommendation is based on the observed trend that there is limited empirical support for the notion that extended runtimes significantly contribute to higher profit margins.

$3.$ To maximize profitability, Microsoft should plan movie releases between April and August. This temporal window has exhibited a historical pattern of yielding the highest average profits for movies. Aligning movie releases with this timeframe could capitalize on favorable market dynamics or consumer behaviors during these months.

$4.$ Further research should be done on the role played by actors, directors on the profitability of the movie.



[Presentation Slides](https://docs.google.com/presentation/d/1B0_ji9WTByNSZRDYcfEIPDTii2ot1JZT-QTXBkkKK-0/edit#slide=id.p)