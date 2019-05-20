---
layout: post
title:  "Django REST with React: setting up React and webpack"
date:   2019-05-20 23:43:45 +0700
categories: [python, django, react]
---

The sweet spot for Django and React is Django REST framework for providing API endpoints.

With React in its own app called “frontend”.

We already know how to create a Django app so let’s do it again:

**Create A new app for React**


```console
	django-admin startapp frontend
```
* For `mo = 1`, the output should be `getMonthName(mo) = "Jan"`,
* For `mo = 0`, the output should be `getMonthName(mo) = "invalid month"`.

Let’s also prepare a directory structure for holding the React components:

```console
	mkdir -p ./frontend/src/components
```
and the static files:

```console
	mkdir -p ./frontend/{static,templates}/frontend
```

