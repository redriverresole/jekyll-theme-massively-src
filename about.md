---
layout: page
title: Jekyll Theme - About - Massively
description: When building a website it's helpful to see what the focus of your site is. This page is an example of how to show a website's focus.
sitemap:
    priority: 0.7
    lastmod: 2017-11-02
    changefreq: weekly
---
## About Red Resole

<span class="image left"><img src="{{ "/images/team/team.png" | absolute_url }}" alt="The Team" /></span>

We are rock climbers with the mission of providing a reliable and local shoe re-soling service in order to keep fellow climbers on the rock. Climbing shoes are expensive, and buying a new pair every time the sole wears out can be frustrating. Let us get your favorite, perfectly fitting shoes back on your feet and feeling brand new.

## The Team

<div class="team-members">
	{% for teammember in site.data.teammembers %}
	{% assign mod2 = forloop.index | modulo: 2 %}

	{% if mod2 == 0 %}
		<span class="image left"><img src="{{ site.url }}/images/team/{{ teammember.image }}.png" alt="{{ teammember.name }}" /></span>
	{% endif %}

	{% if mod2 != 0 %}
		<span class="image right"><img src="{{ site.url }}/images/team/{{ teammember.image }}.png" alt="{{ teammember.name }}" /></span>
	{% endif %}

	<!-- <div class="box"> -->
		<h3>{{ teammember.name }}</h3>
		<p><strong>Hometown: </strong>{{ teammember.hometown }}</p>
		<p><strong>Day Job: </strong>{{ teammember.dayjob }}</p>
		<p><strong>Favorite thing about the Red River Gorge: </strong>{{ teammember.rrg }}</p>
	<!-- </div> -->
	{% endfor %}
</div>