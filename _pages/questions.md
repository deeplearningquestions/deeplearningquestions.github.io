---
layout: archive
title: "Questions"
permalink: /questions/
---


https://deeplearningquestions.github.io/questions/this-is-the-second-question/

Last entries for different tags:

{% assign showtags = "category1, category4" | split: ", " %}
{% for tag in showtags %}
  
  {% assign sorted_questions = site.questions | where: "tags", tag | sort: "date" | reverse %}
  {{ tag }}: {{ sorted_questions[0].title }}  {{ sorted_questions[0].url }} 
  
{% endfor %}
