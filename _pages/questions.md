---
layout: archive
title: "Questions"
permalink: /questions/
---

Here all the questions v2


https://deeplearningquestions.github.io/questions/this-is-the-second-question/

{% for question in site.questions %}
 {{ question.title }}
{% endfor %}

{% assign sorted_questions = site.questions | sort: "date" | reverse %}
{% for question in sorted_questions %}
  <h4>{{ question.title }}</h4>
{% endfor %}


{% assign sorted_questions = site.questions | where: "tags", "category1" | sort: "date" %}
{% for question in sorted_questions %}
  <h4>{{ question.title }}</h4>
{% endfor %}
