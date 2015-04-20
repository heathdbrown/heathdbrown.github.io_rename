---
layout: post
title: "Slow progression into NetDevOps"
description: ""
category: tech
tags: [devops, tech]
---
{% include JB/setup %}
Over, the past year, I have been working on a team and now managing a team, that is made up of only four people, attempting to handle the workload
of provisioning, maintaining, and operating a large complex network.

The team I manage handles: 591 netdevices (firewals, load-balancers) and roughly 8,000 switches (aggregation and top of rack).

These devices are an array of vendors, but for the most part are from the normal big vendors in the networking space.

This is a just a brief glance into what we have been doing to modify culture, workflow, and knowledge around NetDevOps.

Culture by definition is the collection of many things. see (http://en.wikipedia.org/wiki/Organizational_culture) Due to the vastness,
it is one of the more complex variables, but I believe is the outcome and not something you can "change". Culture change happens
organically, and by updating values, beliefs, fundamentals etc. of the team.  Culture also is comprised of the types of people,
the managers style, and the engagement of the team.  I say this to make the point of the changes in culture don't happen because
we actively seek to change culture, they change because we actively seek to change the fundametals of what makes up the culture.

Changing the fundametals

When we started the majority of the team did not know what "git" or "github" was besides what some of the other groups sent troubleshooting gists urls.  We began with a simple change, the manual cli changes we were doing, put in a merge request so someone can review the change.  This quickly brought up the requirement to know the basics fo git and the github setup.  The team began to function in this model for a few months.
