---
layout: default
title: "Assignments"
---
 
## {{ site.course.number }} Assignments 

Assignments will be added below.  Readings should be done by the beginning of class.  Exercises should 
be completed by the date and time listed.  Class notes are for your reference of if you have to miss a class.

{% comment %} Jekyll 2.4 doesn't support the concat filter so we hack it with push {% endcomment %}


 
{% comment %} Get exercises and inclass exercises {% endcomment %}
{% assign exercises = "" | split: "" %}
{% assign inclassexercises = "" | split: "" %}
{% assign sortedex = "" | split: "" %}
{% for post in site.posts %}
    {% if post.categories contains "exercise" %}
        {% assign sortedex = sortedex | push: post} %}
    {% endif %}
{% endfor %}
{% for exercise in sortedex %}
    {% if exercise.published != false %}
        {% if exercise.inclass == true %}
            {% assign inclassexercises = inclassexercises | push: exercise %}
        {% else %}
            {% assign exercises = exercises | push: exercise %}
        {% endif %}
    {% endif %}
{% endfor %}

{% comment %} Get readings {% endcomment %}
{% assign readings = (site.categories.reading |  sort: 'date'} %}

{% comment %} Get notes {% endcomment %}
{% assign notes = (site.categories.notes |  sort: 'date'} %}

{% comment %} Push them onto assignments in the correct order {% endcomment %}
{% assign assignments = "" | split: "" %}
{% assign class_dates = "" | split: "" %}
{% for note in (site.categories.notes | sort: 'date') %}
    {% assign class_dates = class_dates | push: note.date %}
{% endfor %}
{% for date in class_dates %}
    {% for reading in readings %}
      {% if reading.date  == date %}
          {% assign assignments = assignments | push: reading %}
      {% endif %}
    {% endfor %}
    {% for exercise in exercises %}
      {% if exercise.date  == date %}
      {% assign assignments = assignments | push: exercise %}
      {% endif %}
    {% endfor %}
    {% for note in notes %}
        {% if note.date == date %}
        {% assign assignments = assignments | push: note %}
        {% endif %}
    {% endfor %}
    {% for ice in inclassexercises %}
      {% if ice.date == date %}
      {% assign assignments = assignments | push: ice %}
      {% endif %}
    {% endfor %}

{% endfor%}

{% assign all_assignments = assignments  %}

<table>
  
    <th>Type</th>
    <th>Title</th>
    <th>Due Date</th>
  
{% for post in all_assignments  %}
    <tr>
        <td>
            {% if post.categories contains "exercise" %}
            <span class="label round {% if post.inclass == true %}warning">In-class {% else %}success">{% endif %}Exercise</span>
            {% endif %}
            {% if post.categories contains "reading" %}
            <span class="label round info">Reading</span>
            {% endif %}
            {% if post.categories contains "notes" %}
            <span class="label round">Class Notes</span>
            {% endif %}
        </td>
        <td>
            {% if post.link %}
                {% assign link = post.link %} 
            {% else %}
                {% capture link %}
                    {{ site.baseurl }}{{ post.url }}{% endcapture %}
            {% endif %}
            <a href="{{ link }}">{% if post.categories contains "notes" %} {{ post.date | date: "%b %d" }} - {% endif %}{{ post.title }} </a>
        </td>
        <td>
            {% if post.categories contains "notes"%}
            {% else %}
            <span>{{ post.date | date: "%a, %b %d, %Y" }} {% if post.categories contains "exercise" %}{% if post.inclass == true %} by midnight{% else %} at {{ post.date | date: "%I:%M %p" }}{% endif %}{% endif %}</span>
            {% endif %}
        </td>
    </tr>
 
{% endfor %}
</table>
