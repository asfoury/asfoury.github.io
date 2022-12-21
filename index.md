---
layout: default
---

# The Streaming war 

Streaming services’ market is considerably growing each year. They are revolutionizing the movie industry. For a long period of time, Netflix was dominating the market in all aspects. Now the streaming war is raging on. The King is being overtaken by growing competitors like Disney plus, Amazon Prime and HBO. To come on top of this furious battle, each streaming service is now launching its own content in addition to acquiring old content. For consumers, choosing which streaming platform to subscribe to is becoming harder than ever. Our goal is to provide insights on which platform offers the best value for movie lovers and help users make informed decisions when choosing a streaming service. We will focus on analyzing movies available on Netflix and Amazon Prime to determine which platform offers a better selection. We will be using data on movie ratings, duration, genre and other relevant features to compare the two platforms.

![movie_ss](assets/images/movies_ss.png)  
*[source](https://blog.reelgood.com/which-streaming-service-offers-the-best-bang-for-your-buck)*


# Where's your favorite movie?

As streaming platforms continue to grow and evolve, it can be difficult to keep track of what movies are available on which platforms. Netflix and Amazon Prime don't provide data about the movies they are offering. Addintionaly, there are no up to date datasets about movies on different platform. Therefore, we decided to take matters into our own hands.

To construct our dataset, we used the IMDb movie data and augmented it with information on which streaming services each movie was available on, using the MovieDB API. For each movie in the IMDb dataset, we made a call to the API to check which streaming platforms it was available on. 

![construction](assets/images/construction.jpeg)  

We then explored our obtained dataset and decided to focus our analysis on the US market, where the competition between streaming platforms is fierce. After looking at the various streaming services, we found that we had the most data for movies available on Netflix and Amazon Prime. In total, we ended up with 6981 movies for Amazon Prime and 2915 movies for Netflix. If we assume that the movie offerings on these two platforms did not change, we would have access to 99% of movies on Prime and 60% of movies on Netflix. In the following sections of our data story, we'll explore how we can handle this issue and compare the movies on these platforms in more detail.

-- INFO, PLOTS ABOUT MOVIES ON US COMPARED TO MOVIES ON OTHER COUNTRIES, PLOTS COMPARINF NUMBER OF MOVIES ON AMAZON AND PRIME

In the following sections, we'll delve deeper into the data and compare the ratings, genres, and other features of the movies on Netflix and Amazon Prime to see which platform offers the best value for movie lovers. Stay tuned to see the results of our analysis!


# Let's explore and compare both platforms

Several factors can be considered when comparing Amazon Prime and Netflix movies


Maps
Netflix in general has more international movies than Prime

### Runtime in minutes, Release Year and Number of Votes Distribution, 
{% include features_before_matching.html %}

### IMDB Rating Distribution
To measure the quality of the movies on each platform, we decided to use the IMDb rating as our metric. IMDb ratings are well known and widely used to decide which movies to watch

{% include ratings_before_matching.html %}

Netflix in general seems to have higher average IMDB ratings than Amazon Prime.


## Hypothesis and Strategy motivation


# Observational Study
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

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
