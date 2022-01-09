---
layout: page
title: Topics and due dates
nav_order: 5
description: Listing of course modules and topics.
---

# Course Calendar (Topics and due dates)

See the [Schedule and Roadmap]({{site.url}}/{{site.baseurl}}/success/#time-management-and-scheduling) suggestions. 

In our course, each week covers roughly 1 chapter, and we have the following course activities: **PA** (Participation Activities), **CA** (Challenge Activities), **LA** (Lab Activities).

{% for module in site.modules %}
{{ module }}
{% endfor %}
