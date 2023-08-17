---
layout: page
title: Works
---
<br><br><br>
<ul>
	<li> <a href="/Portfolios/project_1/" target="_blank">Project Name</a> </li>
</ul>

<!-- <h3>Pick a Category</h3> -->

{% for category in site.categories %}
    {% capture category_name %}{{ category | first }}{% endcapture %}
    <div id="{{ category_name | slugize }}">
    <h3 class="category-head">{{ category_name }}</h3>
    <ul>
      {% for work in site.categories[category_name] %}
          <li><a href="{{ site.baseurl }}{{ work.url }}">{{work.title}}</a></li>
      {% endfor %}
    </div>
    </ul>
{% endfor %}
