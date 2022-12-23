---
layout: default
---

<center> <h1>Does Netflix have better quality movies than Amazon Prime?</h1> </center>

# A fierce war 

Streaming services’ market is considerably growing each year. They are revolutionizing the movie industry. For a long period of time, Netflix was dominating the market in all aspects. Now the streaming war is raging on. The King is being overtaken by growing competitors like Disney plus, Amazon Prime and HBO. To come on top of this furious battle, each streaming service is now launching its own content in addition to acquiring old content. For consumers, choosing which streaming platform to subscribe to is becoming harder than ever. Our goal is to provide insights on which platform offers the best value for movie lovers and help users make informed decisions when choosing a streaming service. We will focus on analyzing movies available on Netflix and Amazon Prime to determine which platform offers a better selection. We will be using data on movie ratings, duration, genre and other relevant features to compare the two platforms.

{% include number_of_movies_per_platform.html %}


# Where's your favorite movie?

As streaming platforms continue to grow and evolve, it can be difficult to keep track of what movies are available on which platforms. Netflix and Amazon Prime don't provide data about the movies they are offering. Addintionaly, there are no up to date datasets about movies on different platform. Therefore, we decided to take matters into our own hands.

To construct our dataset, we used the IMDb movie data and augmented it with information on which streaming services each movie was available on, using the MovieDB API. For each movie in the IMDb dataset, we made a call to the API to check which streaming platforms it was available on. 

![construction](assets/images/construction.jpeg)  

We then explored our obtained dataset and decided to focus our analysis on the US market, where the competition between streaming platforms is fierce. After looking at the various streaming services, we found that we had the most data for movies available on Netflix and Amazon Prime. In total, we ended up with 6981 movies for Amazon Prime and 2915 movies for Netflix. If we assume that the movie offerings on these two platforms did not *[change](https://blog.reelgood.com/which-streaming-service-offers-the-best-bang-for-your-buck)*, we would have access to 99% of movies on Prime and 60% of movies on Netflix. In the following sections of our data story, we'll explore how we can handle this issue and compare the movies on these platforms in more detail.



-- INFO, PLOTS ABOUT MOVIES ON US COMPARED TO MOVIES ON OTHER COUNTRIES, PLOTS COMPARINF NUMBER OF MOVIES ON AMAZON AND PRIME

In the following sections, we'll delve deeper into the data and compare the ratings, genres, and other features of the movies on Netflix and Amazon Prime to see which platform offers the best value for movie lovers. Stay tuned to see the results of our analysis!


# Let's explore and compare both platforms

Several factors can be considered when comparing Amazon Prime and Netflix movies

### International movies
{% include worldmap.html %}
# [🔎 🗺️](another-page.md)
Netflix in general has more international movies than Prime

### Genres Radar Chart 
{% include radar.html %}

We can see that the genres are distributed in a similar way on both platforms, with the two streaming services having more drama movies than any other genre.


### Writers and Directors Distribution
{% include directors.html %}
### Production Companies Map

### Runtime in minutes, Release Year, Number of Votes and The sentiment
{% include features_before_matching.html %}



### Sentiment & Topics on Prime and Netflix

Are you ready to dive into the world of movie ratings? In our research, we set out to compare the quality of movies on Netflix and Amazon Prime. To do this, we examined the descriptions of the movies on each platform.

One aspect of movie descriptions that can be helpful in analyzing their quality is sentiment. Sentiment is made up of two values: polarity and subjectivity. Polarity refers to how positive or negative a movie's description is, while subjectivity measures how objective or subjective it is.

We plotted the distribution of polarity and subjectivity for movies on both Netflix and Amazon Prime, and found that Prime had slightly more negative movie descriptions than Netflix. This difference in distribution could potentially impact the ratings of movies on the two platforms. For example, it's possible that movies with a "negative" feeling are rated lower overall, or vice versa.

To ensure that our comparison of movie ratings on Netflix and Prime was as unbiased as possible, we decided to take the polarity of the movies into account in our observational study. We also considered using subjectivity to select movies for our study, as objective descriptions (with a subjectivity score close to zero) would be more reliable to analyze. However, limiting our selection to movies with low subjectivity would have left us with too few films, compromising the robustness of our study. As a result, we did not include subjectivity in the rest of our analysis.

{% include sentiments.html %}
<br/><br/>

To gain a deeper understanding of the movies on Netflix and Amazon Prime, we used a technique called Latent Dirichlet Allocation (LDA) to extract topics from their descriptions. After extracting twelve topics, we calculated the distribution of these topics for each movie on each platform.

When we plotted the results, we found that the distribution of topics for Netflix and Amazon Prime was almost exactly the same. This could be due to a weak LDA model, or it could be that the selected topics weren't specific enough to differentiate between the two platforms.

In order to observe a difference in the distribution of topics between Netflix and Prime, each topic would need to represent a specific genre and the movie descriptions would need to match this genre in the LDA model. Since the distribution of topics was similar on both platforms, we did not consider them in our observational study.

{% include topic_distribution.html %}

Add comment here
![topics](assets/images/wordcloud.png)

## Hypothesis and Strategy motivation

### IMDB Rating Distribution and Number of Votes Distribution
IMDb is a great resource for film ratings, as users can rate movies on a scale of 1 to 10. These ratings are then used to calculate a weighted average for each film, series, and so on.

But how do we know that these ratings are accurate and legitimate? IMDb uses filters to ensure the integrity of their ratings, though the specific method for doing so is kept confidential to prevent manipulation of the system.

It's also worth noting that the weighted average may sometimes differ significantly from the arithmetic mean due to these filters. So, next time you're looking for a new movie to watch, don't forget to check out the ratings on IMDb!

{% include ratings_before_matching.html %}

In general, Netflix movies have higher frequency of average rated movies than Amazon Prime. Is this comparison reliable?
Is it valid to compare a comedy movie with an action movie? Is it valid to compare a 1 
hour movie with a 3 hours movie? 

These are all confounding variables that complicate the interpretation of our study results to determine if Netflix 
has really higher quality of movies.


# Observational Study

Matching is a useful tool for helping to control for confounding variables in observational studies, 
which can help to increase the validity and reliability of the study results.

### Features after matching
{% include features_after_matching.html %}
### Matching without directors
{% include ratings_after_matching.html %}
### Matching directors 
{% include ratings_after_matching_director.html %}

# Conclusion

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.
