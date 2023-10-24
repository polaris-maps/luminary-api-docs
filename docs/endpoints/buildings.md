---
layout: default
title: Buildings
parent: Endpoints
nav_order: 2
---

# Buildings
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

### /app/ (GET)

#### Request cURL
```
curl https://accessnav-api-git-ctine987.apps.cloudapps.unc.edu/app/building/all
```

#### Response body
{% raw %}
```
[
    {
        "_id": "625e4021000fa59c306e2bc0",
        "name": "Art Studio Building",
        "abbreviation": "LA",
        "defaultLatitude": 35.93180563,
        "defaultLongitude": -79.05819518,
        "campus": "UNC Chapel Hill",
        "__v": 0
    },
    {
        "_id": "625e43d481807ff3dc5f15f5",
        "name": "Kenan Laboratories",
        "abbreviation": "KL",
        "defaultLatitude": 35.90913912,
        "defaultLongitude": -79.05112771,
        "campus": "UNC Chapel Hill",
        "__v": 0
    }
]
```
{% endraw %}