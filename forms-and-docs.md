---
layout: default
title: Policies, forms and documents 
---

<article id="main">
    <header class="special container">
        <span class="icon fa-futbol-o"></span>
        <h2>Policies, forms and documents</h2>
    </header>
    <section class="wrapper style4 container">



        {% for docsection in site.data.docsections %}
        <h3><a id="{{ docsection.title | slugify }}">{{ docsection.title }}</a></h3>
        <ul>
          {% for doc in site.data.docs %}
		{% if doc.group == docsection.section %}
            <li>
		<a href="{{ doc.link }}">{{ doc.description }} ({{ doc.filetype }})</a> <br />
            </li>
		{% endif %}
          {% endfor %}
        </ul>
        {% endfor %}

    </section>
</article>

