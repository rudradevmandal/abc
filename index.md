---
layout: default
title: Home
nav_order: 1
description: "Simplifying groundbreaking research papers."
permalink: /
---

# Welcome to Dumb it Down!

Here at Dumb it Down, we attempt to tackle the notion of boring research papers to an interesting one. We take a research paper that has a significant impact on the progress of science and break it into simpler segments which are fun to read and easy-to-understand, with a pinch of humor baked into it. In short, we simplify groundbreaking research papers.

## To Our Readers
We would like to take this time to clear out few of the misconceptions. We do not assume any ability to understand math and physics, although, it would help if you have sat through a few classes of basic calculus *(I do tend to go into the nits and grits of the topic)*. Even if the math seems incomprehensible, I assure you that it would not hamper your reading as every concept is expanded into very simple, intresting and readable chunks. Please feel free to drop a message to me, in case of any doubts, mistakes in the article or a casual hello!

**Happy Reading!!**


<button class="btn js-toggle-dark-mode">Click to Enter the Dark Side</button>

<script>
const toggleDarkMode = document.querySelector('.js-toggle-dark-mode');

jtd.addEvent(toggleDarkMode, 'click', function(){
  if (jtd.getTheme() === 'dark') {
    jtd.setTheme('light');
    toggleDarkMode.textContent = 'Click to Enter the Dark Side';
  } else {
    jtd.setTheme('dark');
    toggleDarkMode.textContent = 'Take me to the Bright Side';
  }
});
</script>
