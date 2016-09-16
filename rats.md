---
title: Rats
nav: true
layout: default
---

<h2>Bucks</h2>

{% for rat in site.rats %}
{% if rat.gender == "buck" %}

<div class="rat">


{% if rat.image %}
<img src="{{ rat.image }}" />
{% endif %}

<div>

<h3>{{ rat.title }}</h3>

{% if rat.sire %}
<strong>Sire:</strong> {{ rat.sire }}<br />
{% endif %}

{% if rat.dam %}
<strong>Dam:</strong> {{ rat.dam }}
{% endif %}

<p>{{ rat.description }}</p>

</div>

</div>

{% endif %}
{% endfor %}

<hr />

<h2>Does</h2>

{% for rat in site.rats %}
{% if rat.gender == "doe" %}

<div class="rat">


{% if rat.image %}
<img src="{{ rat.image }}" />
{% endif %}

<div>

<h3>{{ rat.title }}</h3>

{% if rat.sire %}
<strong>Sire:</strong> {{ rat.sire }}<br />
{% endif %}

{% if rat.dam %}
<strong>Dam:</strong> {{ rat.dam }}
{% endif %}

<p>{{ rat.description }}</p>

</div>

</div>

{% endif %}
{% endfor %}
