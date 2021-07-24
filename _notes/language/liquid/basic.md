---
doc: https://shopify.github.io/liquid/basics/introduction/
update: 2021-07-24
---

{% raw %}

## Syntax

To render objects or variables, use double curly braces.

```liquid
{{ page.title }}
```

for logic and flow control, use curly brace percentage delimiters.

```liquid
{% if user %}
  Hello {{ user.name }}!
{% endif %}
```

{% endraw %}
