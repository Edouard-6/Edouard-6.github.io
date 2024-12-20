---
date: 2012-03-21 12:26:40
layout: post
title: Will your movie be successful?
description: Ever wondered what it would feel like to be an award winning movie producer? Find out using our success calculator
image: https://res.cloudinary.com/df2o3hsmr/image/upload/v1734726782/1355172_zu7wwn.png
optimized_image: https://res.cloudinary.com/df2o3hsmr/image/upload/v1734726782/1355172_zu7wwn.png
category: Success Calculator
order: 6
tags:
  - Calculator
  - Movie success
author: Serge El Asmar
---

Have fun exploring what rating or ROI you would get if you were your very own movie producer. Sadly, this calculator has very limited predictive power due to its low amount of variables. This is because the regression model had too many insignificant categorical variables. This can nevertheless remain a first estimate of your movie's performance!

<div class="post-interactive-calculator">
  <div id="regression-calculator">
    <h2>Movie Success Calculator</h2>
    <form id="regression-form">
      <label for="regression-choice">Select metric to calculate:</label>
      <select id="regression-choice" name="regression">
        <option value="regression1">ROI</option>
        <option value="regression2">Rating</option>
      </select>
      <br /><br />

      <label for="female-actors">Number of Female Actors:</label>
      <input type="number" id="female-actors" name="female-actors" required />
      <br />

      <label for="male-actors">Number of Male Actors:</label>
      <input type="number" id="male-actors" name="male-actors" required />
      <br />

      <label for="movie-runtime">Movie Runtime (minutes):</label>
      <input type="number" id="movie-runtime" name="movie-runtime" required />
      <br />

      <label for="is-not-only-english">Is your movie only available in English?</label>
      <input type="checkbox" id="is-not-only-english" name="is-not-only-english" />
      <br />

      <label for="is-usa-movie">Is your movie only available in the USA?</label>
      <input type="checkbox" id="is-usa-movie" name="is-usa-movie" />
      <br /><br />

      <button type="button" onclick="calculate()">Calculate</button>
    </form>
    <div id="result" style="margin-top: 20px; font-weight: bold; color: #0073e6;">
      <!-- Result will be displayed here -->
    </div>
  </div>
</div>