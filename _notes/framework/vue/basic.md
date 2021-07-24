---
doc: https://vuejs.org/v2/guide/index.html
update: 2021-07-24
---

{% raw %}

## Variable rendering

Any javascript is valid inside vue directives

```html
<div id="app">
  {{ message }}
</div>
```

```javascript
var app = new Vue({
  el: '#app',
  data: {
    message: 'Hello Vue!'
  }
})
```

## Attribute binding

```html
<div id="app">
  <span v-bind:title="message">
    Hover me.
  </span>
</div>
```

```javascript
var app = new Vue({
  el: '#app',
  data: {
    message: 'You loaded this page on ' + new Date().toLocaleString()
  }
})
```

## Event

```html
<div id="app">
  <p>{{ message }}</p>
  <button v-on:click="reverseMessage">Reverse Message</button>
  <button v-on:click="calculate(param1, param2)">Calculate</button>
</div>
```

```javascript
var app = new Vue({
  el: '#app',
  data: {
    message: 'Hello Vue.js!'
  },
  methods: {
    reverseMessage: function () {
      this.message = this.message.split('').reverse().join('')
    }
    calculate: function (param1, param2) {
      this.message = param1 + param2
    }
  }
})
```

## Input-variable binding

```html
<div id="app">
  <p>{{ message }}</p>
  <input v-model="message">
</div>
```

```javascript
var app = new Vue({
  el: '#app',
  data: {
    message: 'Hello Vue!'
  }
})
```

{% endraw %}
