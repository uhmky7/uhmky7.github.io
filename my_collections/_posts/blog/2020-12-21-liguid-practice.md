---  
title: "Liguid Practice"  
excerpt: "yml로 된 파일이나 md 같은 markdown언어연습 "  
sidebar_main: true
date_show: false  
toc: true
toc_sticky: true
toc_label: "페이지 주요 목차"     
categories:  
   - Blog  
tags:  
   - liguid  
product: "Awesome Shoes"
---  
  
## Tags / Comment

Anything you put between {% comment %} and {% endcomment %} tags
is turned into a comment.

## Tags / Control flow
 {% for post in collections.product %}
{{ portfolio.baz-boom-identity.title }}
{{ baz-boom-identity.title }}
{{ portfolio.title }}
{{ collections_product.title }}
{{ collections.product.title }}
{{ product.title }}
{{ shoes.title }}
{% capture product.title %}Awesome Shoes{% endcapture %}
 {% endfor %}

{{ product.title }}

{% if product.title == "Awesome Shoes" %}
  These shoes are awesome!
{% endif %}

---

{% if page %}
  Hello {{ page.title }}!
{% endif %}

---
## Tags / Variable

#### assign

{% assign my_variable = false %}
{% if my_variable != true %}
  This statement is valid.
{% endif %}
{% assign my_variable = true %}
{% if my_variable == true %}
  This statement is not valid.
{% endif %}

---

{% assign foo = "bar" %}
{{ foo }}


#### capture

{% capture me_variable %}I am being captured.{% endcapture %}
{{ me_variable }}

---

{% assign favorite_food = "pizza" %}
{% assign age = 35 %}

{% capture about_me %}
I am {{ age }} and my favorite food is {{ favorite_food }}.
{% endcapture %}

{{ about_me }}

---


#### increment

{% increment my_counter %}
{% increment my_counter %}
{% increment my_counter %}

---

{% assign var = 10 %}
{% increment var %}
{% increment var %}
{% increment var %}
{{ var }}

---

{% decrement variable %}
{% decrement variable %}
{% decrement variable %}



