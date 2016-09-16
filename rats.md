---
title: Rats
nav: true
layout: default
---

<h2>Bucks</h2>

{% for rat in site.rats %}
{% if rat.Gender == "Buck" and rat.RIP == null %}

<div class="rat">


{% if rat.Image %}
<img src="{{ rat.Image }}" />
{% endif %}

<div>

<h3>{{ rat.title }}</h3>

{% if rat.DOB %}
<strong>DOB:</strong> {{ rat.DOB }}
{% endif %}

{% if rat.Sire %}
<strong>Sire:</strong> {{ rat.Sire }}<br />
{% endif %}

{% if rat.Dam %}
<strong>Dam:</strong> {{ rat.Dam }}
{% endif %}

<p>{{ rat.Description }}</p>

</div>

</div>

{% endif %}
{% endfor %}

<hr />

<h2>Does</h2>

{% for rat in site.rats %}
{% if rat.Gender == "Doe" %}

<div class="rat">


{% if rat.Image %}
<img src="{{ rat.Image }}" />
{% endif %}

<div>

<h3>{{ rat.title }}</h3>

{% if rat.DOB %}
<strong>DOB:</strong> {{ rat.DOB }}
{% endif %}

{% if rat.Sire %}
<strong>Sire:</strong> {{ rat.Sire }}<br />
{% endif %}

{% if rat.Dam %}
<strong>Dam:</strong> {{ rat.Dam }}
{% endif %}

<p>{{ rat.Description }}</p>

</div>

</div>

{% endif %}
{% endfor %}

<hr />

<h2>Past rats</h2>

{% for rat in site.rats %}
{% if rat.RIP %}

<div class="rat">


{% if rat.Image %}
<img src="{{ rat.image }}" />
{% endif %}

<div>

<h3>{{ rat.title }}</h3>

{% if rat.DOB %}
<strong>DOB:</strong> {{ rat.DOB }}
{% endif %}

<strong>RIP:</strong> {{ rat.RIP }}

{% if rat.Sire %}
<strong>Sire:</strong> {{ rat.Sire }}<br />
{% endif %}

{% if rat.Dam %}
<strong>Dam:</strong> {{ rat.Dam }}
{% endif %}

<p>{{ rat.Description }}</p>

</div>

</div>

{% endif %}
{% endfor %}