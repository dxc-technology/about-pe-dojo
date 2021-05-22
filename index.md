---
layout: home
permalink: /
title: "Online Product Engineering Dojo"
date: 2019-07-26
modified: 2020-04-19
excerpt: "A set of hands on learning modules covering both the cultural aspects and practices of Product Engineering."
image:
  top: home-1600x800.jpg
  feature: home-featured.png
---

## Online Product Engineering Dojo

The <a href="{{ site.url }}/modules">Online Product Engineering Dojo</a> is a novel set of hands on learning modules which cover both the cultural aspects and practices aspects of Product Engineering.

The modules can be run from your browser without any download or configuration. They are hosted on [GitHub](https://github.com/dxc-technology/online-pe-dojo) and executed from the [Katacoda](https://www.katacoda.com/){:target="_blank" rel="noopener"} platform.

The Product Engineering Dojo curriculum, informed by research on how people learn incorporates storytelling and imaginative learning techniques in an effort to help improve student engagement and thus help them achieve the hoped for learning outcomes.

Humans love stories, the urge to tell stories is in our DNA. The <a href="{{ site.url }}/modules">Online Product Engineering Dojo</a> takes a pioneering role-based story telling approach to help achieve hands-on learning at scale.

The <a href="{{ site.url }}/modules">Online Product Engineering Dojo</a> modules are set in the same **Pet Clinic** multi-verse as DXC's Online DevOps Dojo - [https://dxc-technology.github.io/about-devops-dojo/](https://dxc-technology.github.io/about-devops-dojo/).

![](images/onceuponatime.jpg)

The modules place learners in real-world-like scenarios, scenarios where they work with a virtual cast of characters sharing the challenges and aspirations of the **Universal Imports** team as they learn about Product Engineering.

The troupe of characters in team **Universal Imports** are:

|  |  |
| - | - |
| ![Charlie](images/charlie.png) | **C**harlie is the **C**EO of the Universal Imports Group and a technology entrepreneur, investor, and philanthropist. He views the discipline of Product Engineering as being essential to tilting the scales in favour of future successes rather than in favour of future failures. His motto is to "Better to fail fast if you are likely to fail at all" so he is keen to see more work done in the design and prototyping phases of projects. |
| ![Miyagi](images/miyagi.png) | **M**iyagi Product Engineering **C**oach and **M**entor hired by **C**harlie to increase the use of Product Engineering within the United Imports group. **M**iyagi's coaching philosophy is to engage, coach, empower and support the teams he works with thus enabling those teams to solve problems for themselves. |
| ![Adriana](images/adriana.png) | **A**driana is an **A**rchitect working on the R237 control software for Redrum, InGen's revolutionary rocket designed for suborbital flights. She caught the space bug watching the lunar landings on a grainy old TV set and is busy pursuing her passion for all things Space with InGen. **A**driana has an interest in all phases of the Product Engineering life cycle but has a particular interest in architecture for testability. |
| ![Pennyworth](images/pennyworth.png) | **P**ennyworth a **P**roject Manager from the Daily Mentioner national newspaper is a servant leader, he facilitates the work of the teams on the projects he manages. A loyal and longstanding confidant of **C**harlie, **P**ennyworth often acts as **C**harlie's weather wayne, pardon the pun, on new programs like the introduction of Product Engineering to the Universal Imports Group. |
| ![Paulo](images/paulo.png) | **P**aulo is a **P**roduct Owner. **P**aulo is excited by the increasing focus on Product Engineering. He is particularly keen to understand more about approaches to ideation, conceptualization and prototyping in the hope of making improvements in the Pet Clinic's application development process. |
| ![Brenda](images/brenda.png) | **B**renda from the **B**usiness who following a recent foray by the Pet Clinic into Fair Trade pet products is keen to leverage that opportunity to its full potential. **B**renda is keen to understand how Product Engineering principles can be applied to those developments to help ensure the right product are developed for the intended users in the most efficient manner possible. |
| ![Dan](images/dan.png) | **D**an, one of the Pet Clinic development team. During the Pet Clinics' DevOps transformation Dan focused on test-driven development, continuous integration and continuous delivery pipelines. **D**an has been asked to participate in the Universal Imports Product Engineering guild to give a developer's perspective and to help tailor the Product Engineering practices for software development. |
| ![Merida](images/merida.png) | **M**erida, is an offering lead for one of the **m**anaged service offerings of the Universal Imports Group. **M**erida has been asked to participate in the Product Engineering guild to give the perspective of an offering lead and to help tailor the Product Engineering practices for the groups managed services. |

## Experience Product Engineering - Dojo use you must, Luke!

Start your Online Product Engineering Dojo journey with our collection of modules 👇

<div class="wrap">
  <div class="tiles">
    <!-- User 'order' attribute to sort posts -->
    <!-- All posts with an order -->
    {% assign postArray = "" | split:"|"  %}
    {% for item in site.categories.katacoda %}
      {% if item.order %}
        {% if item.tags contains 'test' %}
        {% else %}
          {% assign postArray = postArray | push: item %}
        {% endif %}
      {% endif %}
    {% endfor %}

    {% assign postArray = postArray | sort: 'order'  %}

    <!-- Then all others -->
    {% assign postArrayNoOrder = "" | split:"|"  %}
    {% for item in site.categories.katacoda %}
      {% unless item.order %}
        {% assign postArrayNoOrder = postArrayNoOrder | push: item %}
      {% endunless %}
    {% endfor %}

    {% for post in postArray %}
      {% include post-grid.html %}
    {% endfor %}
    {% for post in postArrayNoOrder %}
      {% include post-grid.html %}
    {% endfor %}
  </div><!-- /.tiles -->
</div><!-- /.wrap -->

## Open Source

The Online Product Engineering Dojo is fully Open Source. Hope on over to the [about section]({{ site.url }}/about#contributing) for more details and guidance for contributions.
