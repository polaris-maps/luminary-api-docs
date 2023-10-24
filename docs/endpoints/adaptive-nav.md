---
layout: default
title: Adaptive Navigation
parent: Endpoints
nav_order: 5
---

# Adaptive Navigation
{: .no_toc }
- *NOTE*: Coordinates should be specified as [longitude, latitude].
- For all possible route options, see types [on GitHub](https://github.com/polaris-maps/luminary-api/blob/main/routes/types.js).
- For quick testing without making POST request, use the [/app/route/hardcoded-test](https://accessnav-api-git-ctine987.apps.cloudapps.unc.edu/app/route/hardcoded-test) route.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

### /app/route
#### Request cURL (Minimal Request)
```
curl -X POST 'https://accessnav-api-git-ctine987.apps.cloudapps.unc.edu/app/route' -H "Content-type: application/json" -d '{
  "coordinates": [[-79.045848, 35.904798], [-79.053061, 35.909575]]
}'
```

#### Request cURL (Detailed Request)
```
curl -X POST 'https://accessnav-api-git-ctine987.apps.cloudapps.unc.edu/app/route' -H "Content-type: application/json" -d '{
  "coordinates": [[-79.045848, 35.904798], [-79.053061, 35.909575]],
    "avoid_features": ["steps"],
    "avoid_obstacles": ["narrow"],
    "restrictions": {
        "surface_type": "cobblestone:flattened",
        "track_type": "grade1",
        "smoothness_type": "good",
        "maximum_incline": 6
    }
}'
```

#### Response body
{% raw %}
```
{
    "type": "FeatureCollection",
    "features": [
        {
            "bbox": [
                -79.053055,
                35.904822,
                -79.045823,
                35.910285
            ],
            "type": "Feature",
            "properties": {
                "segments": [
                    {
                        "distance": 1129,
                        "duration": 804,
                        "steps": [
                            {
                                "distance": 57.2,
                                "duration": 41.2,
                                "type": 11,
                                "instruction": "Head northwest",
                                "name": "-",
                                "way_points": [
                                    0,
                                    3
                                ]
                            },
                            {
                                "distance": 114.6,
                                "duration": 82.5,
                                "type": 1,
                                "instruction": "Turn right",
                                "name": "-",
                                "way_points": [
                                    3,
                                    7
                                ]
                            },
                            {
                                "distance": 39.3,
                                "duration": 28.3,
                                "type": 12,
                                "instruction": "Keep left",
                                "name": "-",
                                "way_points": [
                                    7,
                                    8
                                ]
                            },
                            {
                                "distance": 166.5,
                                "duration": 119.9,
                                "type": 12,
                                "instruction": "Keep left",
                                "name": "-",
                                "way_points": [
                                    8,
                                    17
                                ]
                            },
                            {
                                "distance": 67.4,
                                "duration": 48.5,
                                "type": 12,
                                "instruction": "Keep left",
                                "name": "-",
                                "way_points": [
                                    17,
                                    18
                                ]
                            },
                            {
                                "distance": 202.9,
                                "duration": 142.3,
                                "type": 4,
                                "instruction": "Turn slight left",
                                "name": "-",
                                "way_points": [
                                    18,
                                    29
                                ]
                            },
                            {
                                "distance": 16.1,
                                "duration": 11.6,
                                "type": 0,
                                "instruction": "Turn left",
                                "name": "-",
                                "way_points": [
                                    29,
                                    30
                                ]
                            },
                            {
                                "distance": 120.7,
                                "duration": 81.8,
                                "type": 1,
                                "instruction": "Turn right",
                                "name": "-",
                                "way_points": [
                                    30,
                                    36
                                ]
                            },
                            {
                                "distance": 71.2,
                                "duration": 51.3,
                                "type": 12,
                                "instruction": "Keep left",
                                "name": "-",
                                "way_points": [
                                    36,
                                    38
                                ]
                            },
                            {
                                "distance": 27.9,
                                "duration": 20.1,
                                "type": 0,
                                "instruction": "Turn left",
                                "name": "-",
                                "way_points": [
                                    38,
                                    39
                                ]
                            },
                            {
                                "distance": 151,
                                "duration": 108.7,
                                "type": 13,
                                "instruction": "Keep right",
                                "name": "-",
                                "way_points": [
                                    39,
                                    51
                                ]
                            },
                            {
                                "distance": 62.2,
                                "duration": 44.8,
                                "type": 12,
                                "instruction": "Keep left",
                                "name": "-",
                                "way_points": [
                                    51,
                                    54
                                ]
                            },
                            {
                                "distance": 7.7,
                                "duration": 5.5,
                                "type": 1,
                                "instruction": "Turn right",
                                "name": "-",
                                "way_points": [
                                    54,
                                    55
                                ]
                            },
                            {
                                "distance": 24.3,
                                "duration": 17.5,
                                "type": 0,
                                "instruction": "Turn left",
                                "name": "-",
                                "way_points": [
                                    55,
                                    57
                                ]
                            },
                            {
                                "distance": 0,
                                "duration": 0,
                                "type": 10,
                                "instruction": "Arrive at your destination, on the right",
                                "name": "-",
                                "way_points": [
                                    57,
                                    57
                                ]
                            }
                        ]
                    }
                ],
                "summary": {
                    "distance": 1129,
                    "duration": 804
                },
                "way_points": [
                    0,
                    57
                ]
            },
            "geometry": {
                "coordinates": [
                    [
                        -79.045823,
                        35.904822
                    ],
                    [
                        -79.04584,
                        35.904834
                    ],
                    [
                        -79.046266,
                        35.904928
                    ],
                    [
                        -79.046418,
                        35.90497
                    ],
                    [
                        -79.046379,
                        35.905022
                    ],
                    [
                        -79.046363,
                        35.905077
                    ],
                    [
                        -79.046001,
                        35.905699
                    ],
                    [
                        -79.045952,
                        35.905922
                    ],
                    [
                        -79.046085,
                        35.906258
                    ],
                    [
                        -79.046168,
                        35.90661
                    ],
                    [
                        -79.046206,
                        35.906801
                    ],
                    [
                        -79.046239,
                        35.906987
                    ],
                    [
                        -79.046242,
                        35.907005
                    ],
                    [
                        -79.046263,
                        35.907126
                    ],
                    [
                        -79.046313,
                        35.907226
                    ],
                    [
                        -79.046329,
                        35.907258
                    ],
                    [
                        -79.046432,
                        35.907397
                    ],
                    [
                        -79.046656,
                        35.907652
                    ],
                    [
                        -79.047041,
                        35.908171
                    ],
                    [
                        -79.047077,
                        35.908185
                    ],
                    [
                        -79.04713,
                        35.908205
                    ],
                    [
                        -79.04718,
                        35.908225
                    ],
                    [
                        -79.047684,
                        35.90843
                    ],
                    [
                        -79.048275,
                        35.908548
                    ],
                    [
                        -79.048484,
                        35.908613
                    ],
                    [
                        -79.048606,
                        35.908686
                    ],
                    [
                        -79.048628,
                        35.9087
                    ],
                    [
                        -79.048693,
                        35.908788
                    ],
                    [
                        -79.048705,
                        35.908812
                    ],
                    [
                        -79.048855,
                        35.909081
                    ],
                    [
                        -79.049017,
                        35.909021
                    ],
                    [
                        -79.049052,
                        35.909078
                    ],
                    [
                        -79.049088,
                        35.909135
                    ],
                    [
                        -79.049137,
                        35.909224
                    ],
                    [
                        -79.049446,
                        35.909773
                    ],
                    [
                        -79.049482,
                        35.909834
                    ],
                    [
                        -79.049594,
                        35.91
                    ],
                    [
                        -79.049896,
                        35.910109
                    ],
                    [
                        -79.050302,
                        35.910285
                    ],
                    [
                        -79.050579,
                        35.910173
                    ],
                    [
                        -79.050741,
                        35.91021
                    ],
                    [
                        -79.050777,
                        35.910214
                    ],
                    [
                        -79.050795,
                        35.910213
                    ],
                    [
                        -79.05082,
                        35.910206
                    ],
                    [
                        -79.051068,
                        35.910109
                    ],
                    [
                        -79.051304,
                        35.910021
                    ],
                    [
                        -79.051469,
                        35.909999
                    ],
                    [
                        -79.051743,
                        35.909969
                    ],
                    [
                        -79.051815,
                        35.909965
                    ],
                    [
                        -79.051918,
                        35.909925
                    ],
                    [
                        -79.052128,
                        35.909844
                    ],
                    [
                        -79.052154,
                        35.909834
                    ],
                    [
                        -79.052641,
                        35.909646
                    ],
                    [
                        -79.052696,
                        35.909625
                    ],
                    [
                        -79.052777,
                        35.909593
                    ],
                    [
                        -79.05281,
                        35.909656
                    ],
                    [
                        -79.052947,
                        35.909607
                    ],
                    [
                        -79.053055,
                        35.909565
                    ]
                ],
                "type": "LineString"
            }
        }
    ],
    "bbox": [
        -79.053055,
        35.904822,
        -79.045823,
        35.910285
    ],
    "metadata": {
        "attribution": "openrouteservice.org | OpenStreetMap contributors",
        "service": "routing",
        "timestamp": 1679493379540,
        "query": {
            "coordinates": [
                [
                    -79.045848,
                    35.904798
                ],
                [
                    -79.053061,
                    35.909575
                ]
            ],
            "profile": "wheelchair",
            "format": "geojson",
            "options": {
                "avoid_features": [
                    "steps"
                ],
                "profile_params": {
                    "restrictions": {
                        "surface_type": "cobblestone:flattened",
                        "track_type": "grade1",
                        "smoothness_type": "good",
                        "maximum_incline": 6
                    },
                    "surface_quality_known": false,
                    "allow_unsuitable": false
                },
                "avoid_polygons": {
                    "coordinates": [
                        []
                    ],
                    "type": "Polygon"
                }
            }
        },
        "engine": {
            "version": "6.8.1",
            "build_date": "2023-02-27T01:00:29Z",
            "graph_date": "2023-03-10T14:09:02Z"
        }
    }
}
```
{% endraw %}

### /app/route/minimize-door-distance
Given source and destination building ids (and appropriate constraints), return latitudes/longitudes of valid source and destination doors.

#### Request cURL (Minimal Request)
```
curl -X POST 'https://accessnav-api-git-ctine987.apps.cloudapps.unc.edu/app/route/minimize-door-distance' -H "Content-type: application/json" -d '{
    "source": "625e43d481807ff3dc5f1615",
    "destination": "625e43d481807ff3dc5f15f9"
}'
```

#### Request cURL (Detailed Request)
```
curl -X POST 'https://accessnav-api-git-ctine987.apps.cloudapps.unc.edu/app/route/minimize-door-distance' -H "Content-type: application/json" -d '{
    "source": "625e43d481807ff3dc5f1615",
    "destination": "625e43d481807ff3dc5f15f9",
    "exclude_stairs": true,
    "require_automatic": false
}'
```

#### Response body
{% raw %}
```
{
    "metadata": {
        "attribution": "openrouteservice.org | OpenStreetMap contributors",
        "service": "matrix",
        "timestamp": 1698114826231,
        "query": {
            "locations": [
                [
                    -79.053187,
                    35.909526
                ],
                [
                    -79.052961,
                    35.909809
                ],
                [
                    -79.053554,
                    35.910059
                ],
                [
                    -79.05317,
                    35.9102
                ],
                [
                    -79.05331,
                    35.909694
                ],
                [
                    -79.052948,
                    35.909613
                ],
                [
                    -79.052999,
                    35.909907
                ],
                [
                    -79.053447,
                    35.909896
                ],
                [
                    -79.05309,
                    35.91003
                ],
                [
                    -79.055098,
                    35.912506
                ],
                [
                    -79.050822,
                    35.91312
                ]
            ],
            "profile": "foot-walking",
            "responseType": "json",
            "sources": [
                "0",
                "1",
                "2",
                "3",
                "4",
                "5",
                "6",
                "7",
                "8"
            ],
            "destinations": [
                "9",
                "10"
            ]
        },
        "engine": {
            "version": "7.1.0",
            "build_date": "2023-07-09T01:31:50Z",
            "graph_date": "2023-10-15T21:44:44Z"
        }
    },
    "durations": [
        [
            293.34,
            412.23
        ],
        [
            310.17,
            377.54
        ],
        [
            241.23,
            391.59
        ],
        [
            274.67,
            342.05
        ],
        [
            273.67,
            425.48
        ],
        [
            309.52,
            395.04
        ],
        [
            317.04,
            384.41
        ],
        [
            249.01,
            399.37
        ],
        [
            292.21,
            359.58
        ]
    ],
    "destinations": [
        {
            "location": [
                -79.055097,
                35.912504
            ],
            "snapped_distance": 0.26
        },
        {
            "location": [
                -79.050822,
                35.91312
            ],
            "snapped_distance": 0.06
        }
    ],
    "sources": [
        {
            "location": [
                -79.053185,
                35.909527
            ],
            "snapped_distance": 0.22
        },
        {
            "location": [
                -79.05296,
                35.909809
            ],
            "snapped_distance": 0.13
        },
        {
            "location": [
                -79.053557,
                35.910058
            ],
            "snapped_distance": 0.27
        },
        {
            "location": [
                -79.053164,
                35.910197
            ],
            "snapped_distance": 0.59
        },
        {
            "location": [
                -79.053311,
                35.909696
            ],
            "snapped_distance": 0.3
        },
        {
            "location": [
                -79.05295,
                35.909612
            ],
            "snapped_distance": 0.2
        },
        {
            "location": [
                -79.052996,
                35.909906
            ],
            "snapped_distance": 0.3
        },
        {
            "location": [
                -79.053557,
                35.909851
            ],
            "snapped_distance": 11.04
        },
        {
            "location": [
                -79.053085,
                35.910033
            ],
            "snapped_distance": 0.54
        }
    ]
}
```
{% endraw %}
