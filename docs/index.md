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

|App|Description|Free|Paid|Has API|
| --- | --- | --- | --- | --- |
<!-- | [GitHub](https://github.com/) |  Millions of developers and companies build, ship, and maintain their software on GitHub—the largest and most advanced development platform in the world. . | Yes | Yes | Yes | -->
{% for tool in site.data.tools %}
| [{{ tool.App }}] {{ (tool.Link) }} | {{ tool.Description }} | {{ tool.Free }} | {{ tool.Paid }} | {{ tool.Has_API }} |
{% endfor %}