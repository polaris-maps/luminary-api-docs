---
layout: default
title: Doors
parent: Endpoints
nav_order: 6
---

# Buildings
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

### /app/door/all (GET)

#### Request cURL
```
curl https://accessnav-api-git-ctine987.apps.cloudapps.unc.edu/app/door/all
```

#### Response body
{% raw %}
```
[
    {
        "_id": "6436b54caa69d764fde15155",
        "latitude": 35.909526,
        "longitude": -79.053187,
        "building": "625e43d481807ff3dc5f1615",
        "ramps": [
            "6436b5a2aa69d764fde1515d"
        ],
        "automatic": false,
        "stairs": false,
        "entrance": true,
        "__v": 0,
        "emergency": false,
        "otherAttributes": []
    },
    {
        "_id": "6436b54caa69d764fde15158",
        "latitude": 35.910059,
        "longitude": -79.053554,
        "building": "625e43d481807ff3dc5f1615",
        "ramps": [],
        "automatic": true,
        "stairs": false,
        "entrance": true,
        "__v": 0,
        "emergency": false,
        "otherAttributes": []
    }
]
```
{% endraw %}