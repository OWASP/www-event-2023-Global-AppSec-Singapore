---

title: Schedule & Trainings
layout: event_noheader
permalink: /trainings/

---
# {{page.title}}

#### Training subject to change based on trainer availability and meeting the number of students per trainer request.

## Pricing SGD 1145.00
<!--
1-day course : $1145.00 SGD<br>

All training will be held at Marina Bay Sands Singapore

<br><br>
1-day training courses will be held on October 4, 2023
-->

<section class='training'>
{% if site.data.trainings.size > 0 %}
{% assign trainings = site.data.trainings | sort: 'Title' %}
{% for trainer in trainings %}
<section class="trainer-section" id="{{trainer.SectionId}}">
<hr>
<ul>
<li><h3 class='training-header'>{{ trainer.Title }}<button class="cta-button grey" {%if trainer.Status == 'Postponed' or trainer.Status == 'Canceled' or trainer.Status == 'Booked Out' %}disabled='true' {%endif%} onclick="location.href='{{trainer.URL}}';" style="margin-left:1em;cursor: pointer;max-width=80px;">{%if trainer.Status == 'Postponed' or trainer.Status == 'Canceled' or trainer.Status == 'Booked Out'%}{{trainer.Status}}{%else%}Join Us{%endif%}</button></h3></li>
<li class="training-desc">{{ trainer.Description }}</li>
    <ul>
        {% for tr in trainer.Trainers %}
        <li><div class="training-container"><a href="/trainers/#{{tr.TrainerId}}" title="{{tr.Biography | strip_html}}"><div class="training-image" style="background-image:url('{{tr.Image}}');"></div>{{tr.Name}}</a></div></li>
        {% endfor %}
    </ul>
</ul>
</section>
{% endfor %}
{% endif %}
</section>



<div>
    <div title="Whova event and conference app" id="whova-agendawidget">
        <p id="whova-loading">Loading...</p>
    </div>
    <script src="https://whova.com/static/frontend/xems/js/embed/embedagenda.js?eid=ZNk4IrprrjY59vB8oh4AnxS1AR86-tmwfzGYK3x2rcs%3D&host=https://whova.com&filter_by=track&filter=Training%20-%20October%204" type="text/javascript"  id="embeded-agenda-script">
    </script>
    <div id="whova-wrap" class="whova-wrap-class">
        Powered By
        <a class="brandlink" target="_blank" href="https://whova.com">
            <b>Whova</b>
        </a>
        <br/>
        <a class="whova-emslink brandanchorlink" target="_blank" href="https://whova.com/blog/free-event-planning-software-make-you-rockstar/">
            event planning tools
        </a>
    </div>
</div>

