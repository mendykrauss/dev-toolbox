---
layout: default
title: Home
---

<!-- <div align=center>
    <a href="/">
        <img src="./images/logo-icon.jpg" width="25%" alt="Logo"/>
    </a>
</div>
<div align=center>
    <h2>Welcome to dev-toolbox</h2>
</div> -->

<!-- |App|Description|Free|Paid|Has API|
| --- | --- | --- | --- | --- |
<table>
<th>
<td>
App
</td>
{% for tool in site.data.tools %}
| <a href="{{ tool.Link }}" target="_blank">{{ tool.App }}</a> | {{ tool.Description }} | {{ tool.Free }} | {{ tool.Paid }} | {{ tool.Has_API }} |
{% endfor %} -->

<table>
  {% for row in site.data.tools %}
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