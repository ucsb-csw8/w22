---
layout: page
title: Schedule
description: The weekly event schedule.
---

# Weekly Schedule

See the [Schedule and Roadmap](../success/#time-management-and-scheduling) suggestions. 

In our course, each week covers roughly 1 chapter, and we have the following course activities: **PA** (Participation Activities), **CA** (Challenge Activities), **LA** (Lab Activities).

{% for schedule in site.schedules %}
{{ schedule }}
{% endfor %}
