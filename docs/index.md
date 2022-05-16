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
        <th>App</th>
        <th>Description</th>
        <th>Free</th>
        <th>Paid</th>
        <th>Has API</th>
    </tr>
    {% endif %}
    {% tablerow pair in row %}
    <tr>
        <td><a href="{{ pair[1].Link }}">{{ pair[1].App }}</a></td>
        <td>{{ pair[1].Description }}</td>
        <td>{{ pair[1].Free }}</td>
        <td>{{ pair[1].Paid }}</td>
        <td>{{ pair[1].Has_API }}</td>
    {% endtablerow %}
    <tr>
  {% endfor %}
</table>