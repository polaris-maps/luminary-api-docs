---
layout: default
title: Home
nav_order: 1
description: "Luminary is an open-source project for accessible campus navigation."
permalink: /
---

# Home
{: .fs-9 }
Navigation, for everyone.
{: .fs-6 .fw-300 }

[View the API](https://github.com/polaris-maps/luminary-api){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }
[Luminary Organization](https://github.com/polaris-maps){: .btn .fs-5 .mb-4 .mb-md-0 }

---

People with disabilities face numerous obstacles to accessing campus activities in the form of physical barriers (ex. stairs, broken elevators, steep inclines, sidewalk blockages) and knowledge barriers (e.g. lack of information on accessibility equipment status, confusing signage for accessible routes). This project aims to address knowledge barriers around campus route-finding by crowdsourcing information on obstacles to suggest routes customized to the needs of the specific user.

Browse the docs to learn more about how to use the API.

## Getting started

The project is currently in development! Open a pull request in one of our public repositories to contribute.

## About the project

Luminary is &copy; 2021-{{ "now" | date: "%Y" }}.

### License

Luminary API is distributed by a [GNU General Public License v3.0](https://github.com/polaris-maps/luminary-api/blob/main/LICENSE).

Just the Docs (the theme used to power the website) is distributed by an [MIT license](https://github.com/just-the-docs/just-the-docs/tree/main/LICENSE.txt).

### Contributing

When contributing to this repository, please first discuss the change you wish to make via issue, email, or any other method with the owners of this repository before making a change. 

(Coming soon) Read more about becoming a contributor in [our GitHub repo](https://github.com/polaris-maps).

#### Thank you to the contributors of the Luminary API!

<ul class="list-style-none">
{% for contributor in site.github.contributors %}
  <li class="d-inline-block mr-1">
     <a href="{{ contributor.html_url }}"><img src="{{ contributor.avatar_url }}" width="32" height="32" alt="{{ contributor.login }}"></a>
  </li>
{% endfor %}
</ul>

### Code of Conduct

Luminary is committed to fostering a welcoming community.

[Coming Soon - View our Code of Conduct](https://github.com/polaris-maps) on our GitHub repository.
