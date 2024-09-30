---
layout: page
title: portfolio
permalink: /portfolio/
---

<html>
<head>
    <link rel="stylesheet" href="https://pro.fontawesome.com/releases/v5.0.10/css/all.css" integrity="sha12345blahblahblahblahblah" crossorigin="anonymous">
<style>
</style>
</head>
<body>

{% for project in site.portfolio %}

{% if project.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ project.redirect }}" target="_blank">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>
{% else %}

<div class="project ">
    <div class="thumbnail">
        <a href="{{ site.baseurl }}{{ project.url }}">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>

{% endif %}

{% endfor %}

<div class="contacticon center">
    <a href="mailto:liamthomasbolton@gmail.com"><i class="fas fa-envelope-square"></i></a>
    <a href="https://www.linkedin.com/in/liam-thomas-bolton" target="_blank"><i class="fab fa-linkedin-square"></i></a>
    <a href="https://github.com/lbuk" target="_blank"><i class="fab fa-github-square"></i></a>
</div>
</body>
</html>