---
title: As-is issue tracker
---
<style>
  .wrapper {width: auto; }
  section { width: 75%; }  
</style>

<h2>#as-is issues - Aug 2022</h2>

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
