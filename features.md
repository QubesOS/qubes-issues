---
layout: default
title: Feature Development Progress
permalink: /features/
---

<style>
table, td, th {
    border-width: 1px;
    border-style: solid;
    padding: 10px;
}
</style>

This page tracks the progress of feature development for the Qubes OS Project.

<div class="row">
  <div class="col-lg-12 col-md-12">
    <table class="table">
      <thead>
        <tr>
          <th>Feature Name</th>
          <th>Issue</th>
          <th>Developer(s)</th>
          <th>Status</th>
          <th>Last Update</th>
          <th>See Also</th>
        </tr>
      </thead>
      <tbody>
      {% for feature in site.data.features %}
        <tr>
          <td>
            {{ feature.name }}
          </td>
          <td>
            <a href="https://github.com/QubesOS/qubes-issues/issues/{{ feature.issue }}">{{ feature.issue }}</a>
          </td>
          <td>
          {% if feature.devs%}
            {{ feature.devs }}
          {% else %}
            (none)
          {% endif %}
          </td>
          <td>
          {% if feature.status.code %}
            {% if feature.status.url %}
              <a href="{{ feature.status.url }}">{{ feature.status.code }}</a>
            {% else %}
              {{ feature.status.code }}
            {% endif %}
          {% else %}
            Planning
          {% endif %}
          </td>
          <td>
            <a href="{{ feature.updated.url }}">{{ feature.updated.date }}</a>
          </td>
          <td>
          {% for info in feature.info %}
            {% if info.type %}
              [<a href="{{ info.url }}">{{ info.type }}</a>]
            {% endif %}
          {% endfor %}
          </td>
        </tr>
      {% endfor %}
      </tbody>
    </table>
  </div>
</div>

Notes
-----
* **Feature Name**: An informal name or description for the feature.
* **Current Developers**: `(none)` means that no developer is currently assigned
  to this feature. Developers from the community are highly encouraged to claim
  these features and work on them! (Even if a feature currently has developers
  assigned to it, it's usually the case that help is still wanted.)
* **Status**: See the table below for the meaning of each status term.
* **Last Update**: For in-progress features, this denotes the last *substantive*
  development progress update (not merely the last time there was activity on
  the issue or thread).
* **See Also**: Related discussions, PoCs, or other links.

| Status Term | Meaning                                                                                                 |
|:------------|:--------------------------------------------------------------------------------------------------------|
| Planning    | Feature is being discussed to determine scope and goals; development has not yet begun.                 |
| In progress | Feature is currently being developed.                                                                   |
| PoC         | A proof-of-concept has been successfully created, but more work is required to integrate it with Qubes. |
| Waiting     | Feature is partially complete, but is waiting on the completion of another component.                   |

<br>

