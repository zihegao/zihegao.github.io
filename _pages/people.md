---
layout: page
permalink: /people
title: Team
description: 
nav: true
nav_rank: 2
---
{% assign groups = site.people | sort: "group_rank" | map: "group" | uniq %}
{% for group in groups %}
## {{ group }}

    {% assign members = site.people | sort: "lastname" | where: "group", group %}
    {% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <div class="col-sm-4 col-md-3">
            	{% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                <img src="{{ '/assets/img/' | append: member.profile.image | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            	{% if member.inline == false %}</a>{% endif %}
            </div>
            <div class="team col-sm-8 col-md-9">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h5 class="card-title">{{ member.profile.name }}</h5>
                    {% if member.profile.position %}<h6 class="card-subtitle mb-2 text-muted">{{ member.profile.position }}</h6>{% endif %}
                    <p class="card-text">
                        {{ member.teaser }}
                    </p>
                    {% if member.inline == false %}</a>{% endif %}
                    {% if member.profile.email %}
                        <a href="mailto:{{ member.profile.email }}" class="card-link"><i class="fas fa-envelope"></i></a>
                    {% endif %}
                    {% if member.profile.phone %}
                        <a href="tel:{{ member.profile.phone }}" class="card-link"><i class="fas fa-phone"></i></a>
                    {% endif %}
                    {% if member.profile.orcid %}
                        <a href="https://orcid.org/{{ site.orcid_id }}" title="ORCID"><i class="ai ai-orcid"></i></a>
                    {% endif %}
                    {% if member.profile.scholar_userid %}
                        <a href="https://scholar.google.com/citations?user={{ site.scholar_userid }}" title="Google Scholar"><i class="ai ai-google-scholar"></i></a>
                    {% endif %}
                    {% if member.profile.twitter %}
                        <a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank"><i class="fab fa-twitter"></i></a>
                    {% endif %}
                    {% if member.profile.github %}
                        <a href="https://github.com/{{ member.profile.github }}" class="card-link" target="_blank"><i class="fab fa-github"></i></a>
                    {% endif %}
                    {% if member.profile.website %}
                        <a href="{{ member.profile.website }}" class="card-link" target="_blank"><i class="fas fa-globe"></i></a>
                    {% endif %}
                    <p class="card-text">
                        <small class="test-muted"><i class="fas fa-thumbtack"></i> {{ member.profile.address | replace: '<br />', ', ' }}</small>
                    </p>
                </div>
            </div>
        </div>
    </div>
</p>
    {% endfor %}
{% endfor %}
<br/><br/>

## PhD Students
**Jake Dunham** <a href="mailto:jbd0043@auburn.edu" class="card-link"><i class="fas fa-envelope"></i></a>

PhD student in ECE, Jan 2024 - present 

Bachelor of Electrical Engineering, Auburn University, 2023



**Ohidul Islam** <a href="mailto:ozi0003@auburn.edu" class="card-link"><i class="fas fa-envelope"></i></a>

PhD student in ECE, Jan 2024 - present  

B.S. in Electrical and Electronic Engineering, Shahjalal University of Science & Technology (SUST), Sylhet, Bangladesh, 2021



## Undergraduate Researchers

### Current Members

**Charlotte Brown**
Physics, Auburn University, 2023 - present
<a href="mailto:scb0118@auburn.edu" class="card-link"><i class="fas fa-envelope"></i></a>

**Dhimitri Petro**
Electrical Engineering, Auburn University, 2024 Summer and 2025 Spring - present <a href="mailto:dcp0030@auburn.edu" class="card-link"><i class="fas fa-envelope"></i></a>  
(Supported by the Summer Undergraduate Research Experience ([SURE](https://eng.auburn.edu/news/2024/07/sure-program-provides-undergraduate-students-with-taste-of-graduate-school.html)) Program and 2025-2026 Undergraduate Research Fellowship Award) 

### Past Members

**Benson Jiang**
ECE, Auburn University, 2025 Spring <a href="mailto:bzj0043@auburn.edu" class="card-link"><i class="fas fa-envelope"></i></a>

**Alejandro Matlalcuatzi**
ECE, Auburn University, 2025 Summer (Supported by the Summer Undergraduate Research Experience ([SURE](https://eng.auburn.edu/news/2024/07/sure-program-provides-undergraduate-students-with-taste-of-graduate-school.html)) Program) 

**Beau Blackburn**
ECE, Auburn University, 2025 Summer 

**Ethan Wilson**
Computer Engineering, Cedarville University, 2025 Summer (Supported by the Summer Undergraduate Research Experience ([SURE](https://eng.auburn.edu/news/2024/07/sure-program-provides-undergraduate-students-with-taste-of-graduate-school.html)) Program) 

**Alex Brown**
Electrical Engineering, Auburn University, 2024 Summer and Fall <a href="mailto:kab0182@auburn.edu" class="card-link"><i class="fas fa-envelope"></i></a>  
(Supported by the Undergraduate Research Early Start Award) 

**Beth Dawe**
Computer Engineering, Auburn University, 2024 Summer <a href="mailto:emd0063@auburn.edu" class="card-link"><i class="fas fa-envelope"></i></a>  
(Supported by the Summer Undergraduate Research Experience ([SURE](https://eng.auburn.edu/news/2024/07/sure-program-provides-undergraduate-students-with-taste-of-graduate-school.html)) Program) 

## Group photos

**2025 July**  
<img src="/assets/img/group_members/202507_group_photo.jpeg" width="400">  
From left to right: Zihe Gao, Jake Dunham, Ohidul Islam, Dhimitri Petro, Alejandro Matlalcuatzi, Beau Blackburn, Ethan Wilson

**2024 July**  
<img src="/assets/img/group_members/202407_group_photo.jpg" width="400">  
From left to right: Jake Dunham, Alex Brown, Beth Dawe, Dhimitri Petro, Ohidul Islam, Zihe Gao. (Charlotte is doing a summer internship in Oak Ridge and missed all the fun.)


