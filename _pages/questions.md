---
layout: archive
title: "Questions"
permalink: /questions/
---

Here all the questions v2


https://deeplearningquestions.github.io/questions/this-is-the-second-question/

All questions of "category1"
{% assign sorted_questions = site.questions | where: "tags", "category1" | sort: "date" | reverse %}
{% for question in sorted_questions %}
  <h4>{{ question.title }}</h4>
{% endfor %}


All questions of "category2"
{% assign sorted_questions2 = site.questions | where: "tags", "category2" | sort: "date" | reverse %}
{% for question in sorted_questions2 %}
  <h4>{{ question.title }}</h4>
{% endfor %}

Only the last element of cat1:
{% assign sorted_questions3 = site.questions | where: "tags", "category1" | sort: "date" | reverse %}
{{ sorted_questions3[0].title }}
