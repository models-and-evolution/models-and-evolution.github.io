---
layout: default
title: Models and Evolution 2026 - Organizers
---
<section class="page-header" style="background: linear-gradient(135deg, #1B2A4A 0%, #2C3E6B 50%, #3D5291 100%);">
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-lg-8">
                <div class="content text-center">
                    <h1 class="mb-3 text-white text-capitalize letter-spacing">Members</h1>
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
                        <h2>Program organizers</h2>
                    </div>
                </div>
            </div>
        </div>
        <div class="row">
        {% assign members = site.data.crew | sort_natural: 'name' %}{% for member in members %}
        {% if member.role != nill and member.role == "po" %}
            <div class="col-lg-4 mt30">
                <img src="{{ site.url }}/asset/images/orga/{{ member.photo }}" alt="{{ member.name }}" class="float-left orga">{{ member.name }}
                <p class="orgasocial">
                {% if member.twitter != nil %}<a href="https://twitter.com/{{ member.twitter }}" class="tw" target="_blank"><i class="icon-twitter"></i>{{ member.twitter }}</a><br>{% endif %}
                {% if member.linkedin != nil %}<a href="https://www.linkedin.com/in/{{ member.linkedin }}" class="lnked" target="_blank"><i class="icon-linkedin-squared"></i>{{ member.linkedin }}</a>{% endif %}
                {% if member.employer != nil %}{{ member.employer }}{% endif %}
                </p>
            </div>
        {% endif %}
        {% endfor %}
        </div>
    </div>
</section>




<section class="section-speaker section">
    <div class="container">
        <div class="row section-heading">
            <div class="col-lg-8">
                <div class="heading">
                    <div class="pl-90">
                        <h2>Steering Committee</h2>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="row">
        {% assign members = site.data.crew | sort_natural: 'name' %}{% for member in members %}
            {% if member.role != nill and member.role == "sc" %}
            <div class="col-lg-4 mt30">
                <img src="{{ site.url }}/asset/images/orga/{{ member.photo }}" alt="{{ member.name }}" class="float-left orga">{{ member.name }}
                <p class="orgasocial">
                {% if member.twitter != nil %}<a href="https://twitter.com/{{ member.twitter }}" class="tw" target="_blank"><i class="icon-twitter"></i>{{ member.twitter }}</a><br>{% endif %}
                {% if member.linkedin != nil %}<a href="https://www.linkedin.com/in/{{ member.linkedin }}" class="lnked" target="_blank"><i class="icon-linkedin-squared"></i>{{ member.linkedin }}</a>{% endif %}
                {% if member.employer != nil %}{{ member.employer }}{% endif %}
                </p>
            </div>
            {% endif %}
        {% endfor %}
        </div>
    </div>
</section>


<section class="section-speaker section">
    <div class="container">
        <div class="row section-heading">
            <div class="col-lg-8">
                <div class="heading">
                    <div class="pl-90">
                        <h2>Program Committee</h2>
                    </div>
                </div>
            </div>
        </div>

        <div class="row">
        {% assign members = site.data.crew | sort_natural: 'name' %}{% for member in members %}
        {% if member.role != nill and member.role == "pc" %}
            <div class="col-lg-4 mt30">
                <img src="{{ site.url }}/asset/images/orga/{{ member.photo }}" alt="{{ member.name }}" class="float-left orga">{{ member.name }}
                <p class="orgasocial">
                {% if member.twitter != nil %}<a href="https://twitter.com/{{ member.twitter }}" class="tw" target="_blank"><i class="icon-twitter"></i>{{ member.twitter }}</a><br>{% endif %}
                {% if member.linkedin != nil %}<a href="https://www.linkedin.com/in/{{ member.linkedin }}" class="lnked" target="_blank"><i class="icon-linkedin-squared"></i>{{ member.linkedin }}</a>{% endif %}
                {% if member.employer != nil %}{{ member.employer }}{% endif %}
                </p>
            </div>
        {% endif %}
        {% endfor %}
        </div>
    </div>
</section>