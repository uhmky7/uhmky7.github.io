---
title: "Collections & Product title, name, position"
toc: false
---

{% for product in site.product %}
  <h2>
    <a href="{{ product.url }}">
      {{ product.name }} - {{ product.position }} - {{ product.title }}   
      >> {{ product.relative_path }}  
      >> {{ product.path}} - {{ product.url }}  
      >> {{ product.date }}  -  {{ product.collection }}
    </a>
    {% if product.title == "Awesome Shoes" %}
        These shoes are awesome!  
    {% endif %}
    {% unless product.title == "Awesome Shoes x" %}
        These shoes are not awesome.
    {% endunless %}
  </h2>
     {% if product.name == "sneakers" %}
           Hey Sneakers!
     {% elsif product.name == "slippers" %}
           Hey Slippers!
     {% else %}
           Hi Stranger!
     {% endif %}
  <p>{{ product.content | markdownify }}</p>
{% endfor %}

---not work

{% assign foo = product.name %}
{{ foo }}

{{ product.title }}


---


{% for product in site.product %}
  {{ product.name }}
  <table>
  {% tablerow product in site.product %}
     {{ product.title }}
   {% endtablerow %}
  </table>
{% endfor %}


---

{% for i in (1..10) %}
  {% if i == 9 %}
    {% break %}
  {% else %}
    {{ i }}
  {% endif %}
{% endfor %}

---

{% for i in (1..10) %}
  {% if i == 4 %}
    {% continue %}
  {% else %}
    {{ i }}
  {% endif %}
{% endfor %}

---

{% assign num = 4 %}
{% for i in (1..num) %}
  {{ i }}
{% endfor %}

---

<!--variable number example-->

{% assign num = 4 %}
<table>
{% tablerow i in (1..num) %}
  {{ i }}
{% endtablerow %}
</table>

<!--literal number example-->

<table>
{% tablerow i in (3..5) %}
  {{ i }}
{% endtablerow %}
</table>


---
{% assign filename = "/index.html" %}
{{ "website.com" | append: filename }}


