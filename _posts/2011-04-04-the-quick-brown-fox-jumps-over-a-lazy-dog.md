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
author: Leila Diouri, Serge El Asmar
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

The tension reaches its peak. *How does the presence of gender-diverse casts shape a film's success? Do the numbers speak of a new paradigm?* In this pivotal moment, we turn to the weapons of movie success. *How does the number of Female and Male actors in movies influence ROI and ratings?* 
<iframe src="/assets/html/Gender_across_Metrics.html" width="150%" height="600px" frameborder="0" scrolling="no"></iframe>

From the **Return On Investment (ROI)** standpoint, a general upwards trend can be noticed for both male and female actors. There seems to be a sweetspot for the average number of male and female actors. However, that sweetspot is very different and so is resulting (logarithmic) ROI. One one hand, an average number of 15 female actors produces a peak log(ROI) of 1.619, corresponding to an ROI of **5.04**. On the other hand, double that amount of male actors produces a peak log(ROI) of 2.173, corresponding to an ROI of **8.785**.

Looking at **Normalized Ratings**, we can see the trends are much more constant indicating deeper analysis is necessary.

But *what can we do to relate all of this data to the Return On Investment and the Normalized Ratings? What about all the other factors that may play a role?* A simple analysis like the one above only allows us to say so much about the true relationship between our variables...

Thankfully, our final participant enters the arena: **Linear Regression**!

But before it even gets to chance to breathe, **movie genres** wants to have its final say: "Movies are very different, bunching them all up makes no sense!". And it is right, let us look at the relationship between our data when considering one genre at a time.
<iframe src="/assets/html/By_genre_Gender_across_Metrics.html" width="150%" height="600px" frameborder="0" scrolling="no"></iframe>

For all the genres, Normalized ratings generally remain consistent, requiring again a deeper analysis.

### **Drama and Comedy**
The results resemble the one of the general analysis. For **drama**, the sweet spot for ROI occurs with around 15 female actors, showing a peak log(ROI) of 1.702, corresponding to an ROI of approximately **5.48**. Similarly to the general analysis, the peak for male cast appears much later with around 22 male actors for a log (ROI) of 2.146 corresponding to a ROI of **8.55** for **drama**. For **comedy**, the highest peak is at 24 male actors for a log (ROI) of 1.984 corresponding to a ROI of **7.27**.  

### **Horror, Thriller and Fantasy**
**Horror**, **fantasy** and **thriller** genres have approximatly the same general principle.

### **Action/Adventure**
As expected, the **action/adventure** genre heavily leans toward male dominance. The highest log(ROI) peaks at 2.288 occur with 26 male actors, showing an ROI of nearly **9.85**! However, female representation struggles, with the highest ROI barely surpassing half that of their male counterparts. 


## Falling Action
<img src="https://res.cloudinary.com/ddor52c2q/image/upload/v1734668653/final_scene_katniss_f8ykkt.webp" alt="Final scene Katmiss" style="width: 50%; height: 300px; border: none;"> 

Linear regression is not 


## Resolution
As the credits roll, one conclusion becomes clear: 
### Graph here:












