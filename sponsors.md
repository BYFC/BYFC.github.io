---
layout: post
title: Sponsors
---

We would like to express our thanks to all of the companies listed below that are sponsoring Barming Youth FC teams this year. Without this support it would be much more difficult to provide our players with the kit they need.

{% for team in site.data.teams %}
{% if team.manager != nil %}
<h2 id="{{ team.shortname }}">{{ team.name }}</h2>

{% if team.sponsor != nil %}
<strong>Sponsor: </strong><a href="{{ team.sponsorURL }}">{{ team.sponsor }}</a>
{% if team.sponsor2 %} and <a href="{{ team.sponsorURL2 }}">{{ team.sponsor2 }}</a> {% endif %}
{% endif %}
{% endif %}

{% endfor %}

