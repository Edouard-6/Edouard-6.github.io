---
date: 2012-03-21 12:26:40
layout: post
title: Fifty Shades of Change
subtitle: "From Fifty Shades of Gray to Fifty Shades of Representation"
description: "An exploration of whether the portrayal of women in film is evolving, moving beyond the clichés of romance and desire to more nuanced and empowering roles."
image: https://res.cloudinary.com/ddor52c2q/image/upload/v1734721886/fifty_shades_big_fpncur.webp
optimized_image: https://res.cloudinary.com/ddor52c2q/image/upload/v1734721886/fifty_shades_big_fpncur.webp
category: Social study
order: 5
tags:
  - Sexualization
  - Bechdel test
  - Clustering
  - Representation
authors:
  - Fawzia Zeitoun
---

## Exposition
> “In a world where the portrayal of women in film has often been shaded by stereotypes and sexualization, a quiet revolution is underway. As filmmakers begin to explore deeper, more multifaceted narratives, questions arise about the implications of these portrayals on both representation and audience perceptions. With streaming platforms reshaping how stories are told and consumed, the rules of the game are changing. How will this evolving landscape impact the visibility and depth of female characters, and which films will lead the charge in redefining gender representation on screen?”


## Rising Action
<img src="https://res.cloudinary.com/ddor52c2q/image/upload/v1734722129/shade1_heather_zyieom.png" alt="Header1" style="width: 80%; height: auto; border: none;">
To answer our questions, we set out to first look at women's representation in cinema. Our first stop was the Bechdel dataset - an established datatest about the portrayal of women on screen. This dataset evaluates movies based on the Bechdel Test, which asks three simple yet revealing questions about a film: Does it have at least two named women? Do these women talk to each other? Do they talk about something other than a man?

What trends could we uncover in gender portrayals over time based on this test? And more importantly, does better representation, as measured by the Bechdel Test, actually matter when it comes to a film’s success?
To answer these questions, we dove into the data with linear regression analysis, looking at how the Bechdel Rating correlates with key success metrics such as log_ROI, the rating, and our measure of movie success, and the results were as below:

| **Variable**       | **Coefficient of Bechdel_Rating** | **p-value**      |
|---------------------|----------------------------------|------------------|
| **log_ROI**         | 0.128                            | 0.003            |
| **Rating**          | 0.0001                 | 0.83             |
| **Movie Success**   | 0.0058                           | 0.01             |

The data paints an encouraging picture here. With a positive coefficient (0.128) and a significant p-value (0.003), it’s clear that movies with better representation of women, as measured by the Bechdel Rating, tend to yield higher ROI. In simpler terms, representation is not just socially valuable—it’s financially rewarding too.

But, is the Bechdel test too simple?
Well, movie critics often point out that it's a blunt instrument—it measures only a narrow slice of representation. After all, a movie could pass the Bechdel Test with two women having a brief conversation about, say, a sandwich, and still fail to offer meaningful representation. That’s why we decided to dig deeper, turning to another dataset: Polygraph’s Film Dialogue Dataset.
It has information about characters in movies, along with their gender and the number of words they speak. This allows us to quantify who gets a voice in the story - literally, and unfortunately, women don't seem to have a say.

<iframe src="/assets/html/Gender_Words.html" width="150%" height="600px" frameborder="0" scrolling="no"></iframe>

Men dominate the dialogue in most movies, with a significant cluster around the 70-90% range of words spoken. Women, on the other hand, cluster around 10-30%, reflecting their more limited speaking roles.

## Climax
<img src="https://res.cloudinary.com/ddor52c2q/image/upload/v1734722272/header2_kv20vb.png" alt="Header2" style="width: 100%; height: auto; border: none;">

*Ouf!* Things are getting steamy - but not necessarily in the way we hoped. The data makes it clear - women don't seem to be represented equally in movies. Even when they are given more dialogue or larger roles, the question remains: What about these few instances of representation? What's driving them?

To investigate further, we turned back to the CMU Movie Summary Dataset. We started by analyzing character types to see how female characters were described. Were they heroes, leaders, or experts? Or were they love interests, sexualized figures, or passive participants in the narrative? Unfortunately, the dataset contained just 59 female characters, a sample size too small to draw any meaningful conclusions.

*But things weren't over yet!* Determined to dig deeper, we shifted our focus to plot summaries - a much richer dataset with detailed descriptions of movie narratives.

First, we attempted zero-shot classification using Facebook's BART model to detect sexualization in plot summaries. The idea was simple: Could a LLM classify whether a female character or movie plot leaned toward sexualized portrayals, without explicit labeling? Unfortunately, Facebook’s BART model didn’t deliver. Its ability to pick up on subtle nuances of sexualization was poor, and its classifications often missed the mark.

Realizing we needed a new approach, we shifted gears. Instead of broadly testing for sexualization, we focused on clustering movies based on genre, since context matters. After all, a sex comedy is very different from a family comedy, and the way female characters are portrayed in each could differ immensely. Could that lead the way?

## Falling Action
<img src="https://res.cloudinary.com/ddor52c2q/image/upload/v1734722349/header3_tegagp.jpg" alt="Header3" style="width: 100%; height: auto; border: none;">

With high hopes, we applied clustering techniques to sub-group movies by genre- action/adventure, comedy, drama, and thriller - in the hopes that this would reveal patterns in how women are portrayed across different types of stories. Unfortunately, the results were... underwhelming.
Much like the tension in Fifty Shades of Grey, our exploration into sub-genres left us with more questions than answers. Clustering by sub-genres didn't yield meaningful insights. Instead of highlighting distinct patterns, the results were dominated by random, generic words that failed to differentiate the portrayal of women across sub-genres, as you can see in the five top words from three clusters in the action/adventure genre.

<div style="display: flex; justify-content: center; overflow: hidden; height: 180px; width: 100%;">
  <iframe 
    src="/assets/html/Clusters.html" 
    style="width: 100%; max-width: 1200px; height: 600px; border: none;" 
    frameborder="0" 
    scrolling="no">
  </iframe>
</div>


## Resolution
<img src="https://res.cloudinary.com/ddor52c2q/image/upload/v1734722421/wedding_voptpr.jpg" alt="Wedding" style="width: 60%; height: auto; border: none;">

Just like the layers of complexity in Fifty Shades of Grey, representation in cinema can’t be fully captured by a single dataset or technique. But this isn’t the end - this is just the end of Season 1. We’ve peeled back one layer of the story, but many more remain. Season 2 will bring sharper tools, better datasets, and new perspectives to explore the depths of representation and the nuances of storytelling.

So, much like Christian Grey’s enigmatic final glance, we’ll leave you with a promise: "See you in Season 2!" The story is far from over.










