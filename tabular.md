---
title: Table test
---

<h2>Foo 002</h2>

{% assign row = site.data.problems-asis-01[0] %} 
{{ row | inspect }}

<table>

  {% for row in site.data.problems-asis-01 %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}

    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}
  {% endfor %}

</table>
