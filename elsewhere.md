---
title: Other Areas
source: tree/master/_data/elsewhere
---
<table class="ui tablet stackable table">
  <thead>
    <tr>
      <th>Name</th>
      <th><i class="world icon"></i></th>
      <th><i class="twitter icon"></i></th>
    </tr>
  </thead>
  <tbody>
{% assign locales = site.data.elsewhere | sort %}
{% for locale_hash in locales %}
{% assign locale = locale_hash[1] %}
{% assign locale_name = locale_hash[0] | replace: '_', ' ' %}
    <tr>
      <td>{{ locale_name }}</td>
      <td>{% if locale.website %}<a href="{{ locale.website }}" target="_new">{{ locale.website }}</a>{% endif %}</td>
      <td>{% if locale.twitter %}<a href='https://twitter.com/{{ locale.twitter }}' target='_new'><i class="twitter icon"></i>{{ locale.twitter }}</a>{% endif %}</td>
    </tr>
{% endfor %}
  </tbody>
</table>
