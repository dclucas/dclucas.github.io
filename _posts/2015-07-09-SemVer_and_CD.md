---
layout: post
title:  "Semver and Continuous Delivery"
date:   2015-07-09 23:00:00
categories: ci cd versioning semver rambling
image: /assets/images/15455378803_87c769fe8b_o.jpg
excerpt_separator: <!--more-->
---
# Semver and Continuous Deployment: are they really good buddies?

Don't get me wrong: I love [SemVer](http://semver.org). When consuming stuff, it keeps me sane. When producing stuff, it keeps me honest. And don't get me started with Continuous Deployment.

But it's like when you have two best buddies who are dating and while you hope for the best, well, it ain't gonna last. 

<!--more-->

Semver is meticulous, tidy, reliable. CD is fast-paced, and cannot wait until tomorrow to get things out of the way. Already seeing the personality clash?

Now, say you are running CD in your team and have just hit the 1.0 milestone. You are also delivering to production at least once a day. If you have no patches, does that mean that you will be at version 1.20.0 by the end of month? And at ~ 1.240.0 by the end of year, if no breaking changes were introduced?

To make things harder, what if you are doing feature toggle? When is it that the minor version gets bumped? How do you version interim, toggled-off deployments, as they are not patches either?

Probably, the best solution for that would be to throw the yet-another-standard card for CD versioning, creating a versioning pattern that keeps Semver's ability to communicate improvements and breaking changes in a non-ambiguous way while  making it less awkward for CD teams. And in the meantime, yes, to bite the bullet and work around the problems above, for cases where semver is mandatory (many build tools take it for granted, for example). Care to join the discussion?
