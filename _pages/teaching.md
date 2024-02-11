---
layout: page
title: teaching
permalink: /teaching/
description: 
nav: true

#As a teacher, my goal is to promote the ways in which philosophy can contribute to people's lives. One such way, of course, concerns critical thinking skills, which, prominent in philosophy, are needed everywhere. But equally important are the mental dispositions on which the good practice of philosophy depends, and whose importance elsewhere I think was well expressed by Bertrand Russell: “The mind which has become accustomed to the freedom and impartiality of philosophic contemplation will preserve something of the same freedom and impartiality in the world of action and emotion.” The final contribution isn’t instrumental: a life without philosophy is like one without art. Thus, my mission is to help my students: i) develop thinking, writing, and reading skills; ii) create a disposition to imagine that is not bound by their current beliefs and an ability to entertain viewpoints that aren’t their own; and iii) contemplate and enjoy philosophical questions. 

---


Below you will find syllabi and other materials of some courses I have taught at [Syracuse University](https://thecollege.syr.edu/philosophy/). Besides teaching various iterations of these courses as instructor of record, I also TAed for courses in political theory, ethics and media professions, and human nature, among others. Before, I was a lecturer at [Universidade Federal de Alagoas](https://ichca.ufal.br/pt-br/graduacao/filosofia), where I taught introductory courses in philosophy, critical thinking and scientific methods, and ontology in medieval philosophy. 


In 2023, I received the [Outstanding TA Award](https://graduateschool.syr.edu/about/awards/outstanding-teaching-assistant-award/), which was granted by The Graduate School based on a faculty nomination, recommendation letters by faculty who observed my classes, solicited letters from students, and teaching material. 

Click below to see the syllabi and other materials of the courses I created and taught at Syracuse. 

<div class="teachings grid">

  {% assign sorted_teaching = site.teaching | sort: "importance" %}
  {% for teaching in sorted_teaching %}
  <div class="grid-item">
    {% if teaching.redirect %}
    <a href="{{ teaching.redirect }}" target="_blank">
    {% else %}
    <a href="{{ teaching.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if teaching.img %}
        <img src="{{ teaching.img | relative_url }}" alt="teaching thumbnail">
        {% endif %}
        <div class="card-body">
          <h2 class="card-title text-lowercase" style="color: black;">{{ teaching.title }}</h2>
          <p class="card-text">{{ teaching.description }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if teaching.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="Code Repository">
                <a href="{{ teaching.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
              {% if teaching.github_stars %}
              <span class="stars" data-toggle="tooltip" title="GitHub Stars">
                <i class="fas fa-star"></i>
                <span id="{{ teaching.github_stars }}-stars"></span>
              </span>
              {% endif %}
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  </div>
{% endfor %}

</div>
