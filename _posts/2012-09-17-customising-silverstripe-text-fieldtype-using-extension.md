---
layout: post
title: "Customising SilverStripe Text fieldtype using Extension"
description: ""
category: 
tags: []
---
{% include JB/setup %}

I have this problem that I need to split the page content by paragraphs. Good thing in SilverStripe you can add or create a custom function to an existing class by using the Extension class. Since the Text fieldtype can only use the FirstParagraph method, I created a custom function that can pull the paragraph of the page content by passing a number.

<script src="https://gist.github.com/3735394.js"> </script>

So as you can see we created a Paragraph function that takes an argument for the paragraph number. Then it returns the parapraph to be rendered in the template.

Don't forget to setup this to your _config.php so that It will override the Text class.
<script src="https://gist.github.com/3735628.js"> </script>

So in the template we can now call the custom function. Cool eh?
<script src="https://gist.github.com/3735631.js"> </script>