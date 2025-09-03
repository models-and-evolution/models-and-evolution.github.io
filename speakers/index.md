---
layout: default
title: Models and Evolution - Program
---
<section class="page-header" style="background-image:url(https://www.volcamp.io/asset/images/chainedespuys_header.jpg);">
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-lg-8">
                <div class="content text-center">
                    <h1 class="mb-3 text-white text-capitalize letter-spacing">Workshop program</h1>
                    <div class="divider mx-auto mb-4 bg-white"></div>
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
                        <h2>Detailed program</h2>
                    </div>
                </div>
            </div>
        </div>
        <div class="row">
            <h4 class="mb-0 mt-3">Session 1</h4>
            {% assign speakers = site.speakers | sort_natural: 'session' %}
            {% for speaker in speakers %}{% if speaker.session == 1 and speaker.title != 'TBD' and speaker.title != 'Volcamp team' and speaker.photo != 'none' %}
            <div class="col-lg-12 col-sm-4">
                <div class="speaker-block mb-5">
                    
                    <div class="speaker-info">

                        <h5 class="mb-0 mt-3">{{ speaker.title }}</h5>
                        <h6 class="mb-0 mt-3">Authors: {{ speaker.authors}}</h6>
                        <h6 class="mb-0 mt-3">Presenter: {{ speaker.presenter}}</h6>
                        <h6 class="mb-0 mt-3">{{ speaker.time}}</h6>
                        <p>{{ speaker.abstract }}</p>
                        {% if speaker.presentation %} <a href="{{site.url}}/asset/presentations/{{speaker.presentation}}">Slides</a>{% endif %}
                    </div>
                </div>
            </div>
            {% endif %}{% else %}
                Rien à voir ici.
            {% endfor %}
        </div>
        <hr>
        <div class="row">
            <h4 class="mb-0 mt-3">Session 2</h4>
            {% assign speakers = site.speakers | sort_natural: 'session' %}
            {% for speaker in speakers %}{% if speaker.session == 2 and speaker.title != 'TBD' and speaker.title != 'Volcamp team' and speaker.photo != 'none' %}
            <div class="col-lg-12 col-sm-4">
                <div class="speaker-block mb-5">
                    
                    <div class="speaker-info">

                        <h5 class="mb-0 mt-3">{{ speaker.title }}</h5>
                        <h6 class="mb-0 mt-3">Authors: {{ speaker.authors}}</h6>
                        <h6 class="mb-0 mt-3">Presenter: {{ speaker.presenter}}</h6>
                        <h6 class="mb-0 mt-3">{{ speaker.time}}</h6>
                        <p>{{ speaker.abstract }}</p>
                        {% if speaker.presentation %} <a href="{{site.url}}/asset/presentations/{{speaker.presentation}}">Slides</a>{% endif %}
                    </div>
                </div>
            </div>
            {% endif %}{% else %}
                Rien à voir ici.
            {% endfor %}
        </div>
        <hr>
        
    </div>
</section>