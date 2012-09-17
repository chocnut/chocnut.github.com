---
layout: post
title: "Customising SilverStripe Text fieldtype using Extension"
description: ""
category: 
tags: []
---
{% include JB/setup %}

I have this problem that I need to split the page content by paragraphs. Good thing in SilverStripe you can add custom function to an existing class using Extension. Since in the Text fieldtype we can only use the FirstParagraph method, I created a custom function that can pull paragraphs from the page content.

<script src="https://gist.github.com/3735394.js"> </script>

So as you can see in the above code snippet, the Paragraph function takes an argument of paragraph number and return the content to be display in the template and Oh don't forget to setup your _config.php so that it will override the Text class.

<script src="https://gist.github.com/3735628.js"> </script>

So in the template we can now call the custom function. Cool eh?
<script src="https://gist.github.com/3735631.js"> </script>