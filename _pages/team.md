---
title: Team
layout: default 
permalink: /team/
nav: true
nav_order: 1
---

<!-- Faculty -->
<h2 class="mb-3"><a id="faculty"></a>Faculty</h2>

{% assign members = site.data.team.faculty %}
<ul class="list-unstyled">
<div class="row">
{% for member in members%}
    {% assign ncols = 2 %}
    {% assign i = forloop.index0 | modulo: ncols %}
        <div class="col">
            {%- include team_member.html -%}
        </div>
    {% if i == 1 %}
        </div><div class="row">
    {% endif %}
{% endfor %}
</div>
</ul>

<!-- Students -->
<h2 class="mb-3"><a id="student"></a>Students</h2>

{% assign members = site.data.team.students %}
<ul class="list-unstyled">
<div class="row">
{% for member in members%}
    {% assign ncols = 4 %}
    {% assign i = forloop.index0 | modulo: ncols %}
        <div class="col">
            {%- include team_member.html -%}
        </div>
    {% if i == 1 %}
        </div><div class="row">
    {% endif %}
{% endfor %}
</div>
</ul>

