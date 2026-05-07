---
layout: default
title: Models and Evolution - Program
---
<section class="page-header" style="background: linear-gradient(135deg, #1B2A4A 0%, #2C3E6B 50%, #3D5291 100%);">
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-lg-8">
                <div class="content text-center">
                    <h1 class="mb-3 text-white text-capitalize letter-spacing">Past Editions</h1>
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
            {% for edition in editions %}
                {{edition.year}}
            {% endfor %}
        </div>
    </div>
</section>