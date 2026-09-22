---
layout: default
title: Models and Evolution 2026 - Program
---
<section class="page-header" style="background: linear-gradient(135deg, #1B2A4A 0%, #2C3E6B 50%, #3D5291 100%);">
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-lg-8">
                <div class="content text-center">
                    <h1 class="mb-3 text-white text-capitalize letter-spacing">Workshop program</h1>
                    <div class="divider mx-auto mb-4 bg-white"></div>
                    <p class="text-white mb-0">{{ site.day1 }} {{ site.month }} &middot; Room Torremolinos D &middot; Meli&aacute; Costa del Sol, M&aacute;laga</p>
                </div>
            </div>
        </div>
    </div>
</section>

<section class="section-speaker section">
    <div class="container">
        <div class="row section-heading">
            <div class="col-lg-8">
                <div class="heading">
                    <div class="pl-90">
                        <h2>At a glance</h2>
                    </div>
                </div>
            </div>
        </div>
        <div class="row">
            <div class="col-lg-12">
                <table class="table">
                    <thead>
                        <tr><th>Time</th><th>Session</th></tr>
                    </thead>
                    <tbody>
                        <tr><td>9:15 - 10:30</td><td>Session 1 &middot; Opening and Keynote</td></tr>
                        <tr><td>10:30 - 11:00</td><td><em>Coffee break</em></td></tr>
                        <tr><td>11:00 - 12:45</td><td>Session 2 &middot; Evolution of Digital Twins and Cyber-Physical Systems</td></tr>
                        <tr><td>13:00 - 14:30</td><td><em>Lunch</em></td></tr>
                        <tr><td>14:30 - 15:45</td><td>Session 3 &middot; Evolving Modeling Languages, Tools and Platforms</td></tr>
                        <tr><td>15:45 - 16:15</td><td><em>Coffee break</em></td></tr>
                        <tr><td>16:15 - 17:30</td><td>Session 4 &middot; Evolution in Practice and 20 Years of ME</td></tr>
                    </tbody>
                </table>
                <p><em>Each paper is allotted 20 minutes for the presentation and 5 minutes for questions.</em></p>
            </div>
        </div>
    </div>
</section>

<section class="section-speaker section">
    <div class="container">
        <div class="row section-heading">
            <div class="col-lg-8">
                <div class="heading">
                    <div class="pl-90">
                        <h2>Detailed program</h2>
                    </div>
                </div>
            </div>
        </div>

        {% assign sessions = "1|Opening and Keynote|9:15 - 10:30|Coffee break 10:30 - 11:00;2|Evolution of Digital Twins and Cyber-Physical Systems|11:00 - 12:45|Lunch 13:00 - 14:30;3|Evolving Modeling Languages, Tools and Platforms|14:30 - 15:45|Coffee break 15:45 - 16:15;4|Evolution in Practice and 20 Years of ME|16:15 - 17:30|" | split: ";" %}
        {% assign program = site.speakers | sort: 'order' %}

        {% for s in sessions %}
        {% assign parts = s | split: "|" %}
        {% assign snum = parts[0] | plus: 0 %}
        <div class="row">
            <div class="col-lg-12">
                <h4 class="mb-0 mt-3">Session {{ parts[0] }} &middot; {{ parts[1] }}</h4>
                <h6 class="mb-3 mt-1">{{ parts[2] }}</h6>
            </div>
            {% for item in program %}{% if item.session == snum %}
            <div class="col-lg-12 col-sm-4">
                <div class="speaker-block mb-5">
                    <div class="speaker-info">
                        <h5 class="mb-0 mt-3">{{ item.title }}</h5>
                        {% if item.authors != "TBA" %}<h6 class="mb-0 mt-3">Authors: {{ item.authors }}</h6>{% endif %}
                        {% if item.presenter != "TBA" %}<h6 class="mb-0 mt-3">Presenter: {{ item.presenter }}</h6>{% endif %}
                        <h6 class="mb-0 mt-3">{{ item.time }}</h6>
                        <p>{{ item.abstract }}</p>
                        {% if item.presentation %}<a href="{{ site.url }}/asset/presentations/{{ item.presentation }}">Slides</a>{% endif %}
                    </div>
                </div>
            </div>
            {% endif %}{% endfor %}
        </div>
        {% if parts[3] != "" %}<p class="text-center"><em>{{ parts[3] }}</em></p>{% endif %}
        <hr>
        {% endfor %}

    </div>
</section>
