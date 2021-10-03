---
layout: archive
title: "Questions"
permalink: /questions/
---

1. Search option

https://deeplearningquestions.github.io/questions/this-is-the-second-question/

2. Last entries for different tags:

{% assign showtags = "category1, category4" | split: ", " %}
{% for tag in showtags %}
  
  {% assign sorted_questions = site.questions | where: "tags", tag | sort: "date" | reverse %}
  {{ tag }}: {{ sorted_questions[0].title }}  {{ sorted_questions[0].url }} 
  
{% endfor %}

3. Tag cloud
{% assign tags =  site.questions | map: 'tags' | uniq %}
{% for tag in tags %}
    {{ tag | slugify }}
{% endfor %}


4. List of all questions
{% assign sorted_questions = site.questions | sort: "date" | reverse %}
{% for question in sorted_questions %}
    {{ question.title }}  {{ question.url }} 
{% endfor %}
