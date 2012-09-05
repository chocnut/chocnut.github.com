---
layout: post
title: "How to work with recurring dates in PHP"
description: ""
category: 
tags: []
---
{% include JB/setup %}

Are you're looking for a library that handles recurring date in PHP? Luckily there's one on [github] (https://github.com/justinethier/When){:target="_blank"}.

So here's a quick snippet and scenario on how to use the libary. User select a week number(s) and day(s), They also set the recurring end date or month(s). Here we call until() method that accept datetime and we call byday() method that accept array of days e.g 'MO,'TU' etc. then we call the next() function to loop over the generated dates. So there you go, Hopefully this post helps.

<script src="https://gist.github.com/3616101.js"> </script>