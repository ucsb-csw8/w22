---
layout: page
title: Topics and due dates
nav_order: 5
description: Listing of course modules and topics.
---

# Course Calendar (Topics and due dates)

See the [Schedule and Roadmap]({{site.url}}/{{site.baseurl}}/success/#time-management-and-scheduling) suggestions. 

In our course, each week covers roughly 1 chapter from zyBooks, and we have the following course activities: 
* **PA**{: .label .label-orange }(Participation Activities), 
* **CA**{: .label .label-blue }(Challenge Activities), 
* **LA**{: .label .label-green }(Lab Activities).

Additionally, at the endo of each week, you are asked to reflect on your learning journey that week and submit a **Reflection** linked on Gauchospace.

[Jump to the current week (Week 2)](#week-2){: .btn .btn-blue }

{% for module in site.modules %}
{{ module }}
{% endfor %}
