---
date: 2012-03-21 12:26:40
layout: post
title: The gender games
subtitle: Who will be crowned king of the arena? Happy gender games! May the odds be ever in your favor.
description: Who will be crowned king of the arena? Happy gender games! May the odds be ever in your favor.
image: https://res.cloudinary.com/df2o3hsmr/image/upload/v1734669141/girl-on-fire-the-hunger-games-x6sxdf7zd05tgr54_uxhwk4.jpg
optimized_image: https://res.cloudinary.com/df2o3hsmr/image/upload/v1734669141/girl-on-fire-the-hunger-games-x6sxdf7zd05tgr54_uxhwk4.jpg
category: Linear regression
order: 2
tags:
  - Lin Reg
  - M vs F
author: Leila Diouri
---

## Exposition
> “The arena for the movie industries’ narratives has long been male-dominated. As the viewers of the capitol wonder if a shift is happening, female actors are eager to break through and challenge old expectations. In this battle for relevance and recognition, the stakes are high. Will gender-diverse films find their place at the top of the box office and on [streaming platforms](/a-wonderful-serenity-has-taken-possession-of-my-entire-soul/), or will they remain underappreciated? As the industry fights to redefine what success looks like, gender becomes the ultimate game-changer. ” 


## Rising Action
<img src="https://res.cloudinary.com/ddor52c2q/image/upload/v1734652851/peeta_katniss_1_y88kbz.png" alt="Peeta and Katniss" style="width: 100%; height: auto; border: none;">

As the cannon's roar signals the start of the battle, the question echos: *What fuels the quest to understand gender representation in cinema?* The past holds the clues, and a visual narrative begins to take shape.
<iframe src="/assets/html/Average_Female_Actor_Percentage_Per_Year.html" width="150%" height="600px" frameborder="0"></iframe>

This graph reveals the trajectory of female representation in films from 1980 to 2014. The data reveals fluctuations in the average percentage of female actors in the 80s, with a **gradual upward trend** from the 90s onwards. However, this graph only gives infomation as a proportion of female actors. Let us take a closer look at the distribution of the frequency of female actors vs male actors.
<iframe src="/assets/html/Frequency_Gender.html" width="150%" height="600px" frameborder="0"></iframe>

This barplot shows that both male and female frenquency count have a normal distribution. The peak frequency for female actors occurs at a much lower count of 3 against 8 for male actors. Futhermore, the distribution of female counts is slightly right skewed. This underscores a **disparity in representation**. Therefore, male actors appear to dominate ensemble casts, whilst female actors appear to be represented in smaller numbers. 

As the battle starts, a new participant enters the arena: **movie genres**. *Will they underline a more equitable fight for representation or will they deepen the disparities even more?*
<iframe src="/assets/html/Per_Genre.html" width="150%" height="600px" frameborder="0"></iframe>

This barplot reveals the distribution of average female actor percentages across various movie genres. **Action/adventure** movies show the lowest representation, with female actors averaging just over 20%. In contrast, genres such as **comedy**, **drama**, and **horror** exhibit significantly higher percentages, nearing 35%. These findings suggest that representation is lower in more physical genres such as action/adventure further underlining the narrative of male physical dominance. More emotional genres such as drama have a higher representation of women which is unsurprising considering societal norms that label women as more sensitive.

Like mentioned before, the past holds the clues. With movie genres entering the fight, the viewers wonder: *have they been relevant fighters throughout history?*
<iframe src="/assets/html/By_Genre_Per_Year.html" width="150%" height="600px" frameborder="0"></iframe>

When toggling between genres, distinct patterns emerge regarding the historical representation of female actors. In **drama**, the average female actor percentage has shown consistent growth from the late 1980s, peaking in the early 2000s before a slight decline. **Comedy**, on the other hand, demonstrates more fluctuations but maintains relatively high representation throughout the years.

**Fantasy** tells a different story, with spikes in female representation during specific years, indicating efforts to highlight strong female leads. In contrast, **thriller** and **horror** genres show inconsistency, though **horror** experienced a significant peak around the 2010s.

The **action/adventure** genre remains the most male-dominated, with female representation rarely exceeding 30%. 

> All of these ongoing fights for representation keep the viewers of the capitol on the edge of their seats. The questions still echo, *who truly holds the power in the Gender Games arena?*

## Climax
<img src="https://res.cloudinary.com/ddor52c2q/image/upload/v1734668079/mockingjay_izyz2j.png" alt="Mockingjay" style="width: 100%; height: auto; border: none;">

The tension reaches its peak. How does the presence of gender-diverse casts shape a film's success? Do the numbers speak of a new paradigm? In this pivotal moment, we turn to the weapons of movie success. How does the number of Female and Male actors in movies influence ROI and ratings? 
<iframe src="/assets/html/Gender_across_Metrics.html" width="150%" height="600px" frameborder="0" scrolling="no"></iframe>

From the Return On Investment (ROI) standpoint, a general upwards trend can be noticed for both male and female actors. There seems to be a sweetspot for the average number of male and female actors. However, that sweetspot is very different and so is resulting (logarithmic) ROI. One one hand, an average number of 15 female actors produces a peak log(ROI) of 1.619, corresponding to an ROI of 5.04. On the other hand, double that amount of male actors produces a peak log(ROI) of 2.173, corresponding to an ROI of 8.785.

Looking at Normalized Ratings, we can see the trends are much more constant indicating deeper analysis is necessary.

But what can we do to relate all of this data to the Return On Investment and the Normalized Ratings? What about all the other factors that may play a role? A simple analysis like the one above only allows us to say so much about the true relationship between our variables...

Thankfully, our final participant enters the arena: **Linear Regression**!

But before it even gets to chance to breathe, movie genres wants to have its final say: "Movies are very different, bunching them all up makes no sense!". And it is right, let us look at the relationship between our data when considering one genre at a time.
<iframe src="/assets/html/By_genre_Gender_across_Metrics.html" width="150%" height="600px" frameborder="0" scrolling="no"></iframe>



## Falling Action
<img src="https://res.cloudinary.com/ddor52c2q/image/upload/v1734668653/final_scene_katniss_f8ykkt.webp" alt="Final scene Katmiss" style="width: 60%; height: 300px; border: none;"> 

Linear regression is not convinced with the arguments brought forward by movie genres. It thinks the relationship is much more complex, requiring the careful consideration of a multitude of factors. It suggests looking at the impact that a set of indpendent variables will have on ROI, Normalized Rating and even a combination of both: Movie Success.

The regression results table being large, only an extract with relevant information is shown here.

Let's take it one at a time starting with log(ROI):

| Statistic       | Value       |
|------------------|-------------|
| Dep. Variable    | log_ROI     |
| R-squared        | 0.349       |
| Adj. R-squared   | 0.345       |
| F-statistic      | 72.82       |
| Prob (F-statistic) | 5.25e-154 |

| Variable               | Coefficient | Std. Error | t-Value | p-value  | 
|------------------------|-------------|------------|---------|--------|
| const                  | 0.6998      | 0.024      | 29.620  | 0.000  | 
| Female_actors          | 0.0935      | 0.025      | 3.734   | 0.000  | 
| Male_actors            | -0.0839     | 0.026      | -3.179  | 0.002  | 

It is very interesting to see that contrarily to what was shown in the previous plots, the average number of female actors has a  coefficient that is positive and statistically significant at the 5% significance level. This means that an increase in the average number of female actors leads to a higher Return On Investment. Even more surprisingly, the average number of male actors has a coefficient that is negative and statistically significant at the 5% significance level! These results go against what was seen in previous plots demonstrating that reality is not always what it seems. This leads opens the door for a series of questions. *What could be the underlying reasons for this higher ROI when more female actors are present? Could it be that women are paid less thus reducing the necessary budget? Does sexualization of women attracts more viewers? Or is it just that society has evolved towards increasing gender diversity?*

Let us look next at Normalized Ratings:

| Statistic            | Value         |
|-----------------------|---------------|
| Dep. Variable         | Normalized_Rating |
| R-squared            | 0.249         |
| Adj. R-squared       | 0.243         |
| F-statistic          | 48.58         |
| Prob (F-statistic)   | 1.85e-100     |


| Variable               | Coefficient | Std. Error | t-Value  | p-value   |
|------------------------|-------------|------------|----------|--------|
| const                  | 0.6468      | 0.002      | 308.374  | 0.000  |
| Female_actors          | -0.0073     | 0.002      | -3.306   | 0.001  |
| Male_actors            | 0.0089      | 0.002      | 3.870    | 0.000  |

When looking at Normalized ratings we see opposite results to the log(ROI) results. Both coefficients are still statitically significant at the 5% level, however, their signs are now flipped. *What could be causing this disparity between ratings and ROI? Which metric matters more? Are female actors just less talented? Or are they more severely criticized and judged?* 

Finally, let's combine everything and look at our Movie Success metric:

| Statistic            | Value         |
|-----------------------|---------------|
| Dep. Variable         | Movie_success |
| R-squared            | 0.102         |
| Adj. R-squared       | 0.096         |
| F-statistic          | 16.69         |
| Prob (F-statistic)   | 3.32e-34      |

| Variable               | Coefficient | Std. Error | t-Value  | p-value  |
|------------------------|-------------|------------|----------|--------|
| const                  | 0.5769      | 0.003      | 223.119  | 0.000  |
| Female_actors          | 0.0041      | 0.003      | 1.490    | 0.136  |
| Male_actors            | 0.0079      | 0.003      | 2.800    | 0.005  |

At first glance it would seem these results reconcile the previous two. Indeed, both coefficients have positive signs leading us to believe that we have finally found a metric in which the rise of both genders is beneficial. However, we are quick to notice that the average number of female actors is not statistically significant at the 5% level. This means that the evidence is not strong enough to conclude that this variable has a meaningful effect on the success of a movie... Our metric is not conclusive given the data at hand.


## Resolution
Alas, we are right back where we started. However, we now have a lot more insight on the fearsome Gender Games. From the trends across time, to the variations across genres, we have paired the mightiest opponents we could find. The general concensus is that the victor of the battle comes down to personal opinion. What matters more: Ratings or Return on Investment? One thing is for sure, women have their place in the movie industry. Their recognition has risen with time and will (hopefully) continue to do so. It is important to look ahead and realize that in this world, **there are much worse games to play**.












