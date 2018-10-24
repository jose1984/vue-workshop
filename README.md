# Introduction 

In this workshop we will learn how to develop a web application using [Vue](https://vuejs.org) (pronounced /vjuː/, like view), which is a progressive framework for building user interfaces. We will go through simple use cases until reaching a professional level. Vue is s, it is useful in both small applications and large projects.

If you'd like to learn more about Vue, we've created a workshop suitable for all levels.

## Hello Vue!

Let's start from the scratch, we can use the online tool [Codepen.io](https://codepen.io/) or just creating an empty html file. Include in your html body a Vue bundle from a public CDN or just download it locally.

```html
<!-- development version, includes helpful console warnings -->
<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
```

```html
<div id="app">
  {{ message }} <!-- Binding message -->
</div>
```

Now we are going to initialize our app creating a new Vue instance, the `vm` object just contains two properties for this example, the element selector `el` to select the main `<div id="app">`, and the `data` object where there are all the binding properties.

```javascript
var vm = {
  el: '#app',
  data: {
    message: 'Hello Vue!'
  }
}

var app = new Vue(vm)
```

Follow the example [here](./Application/example-1.html).

## Resume

When we say Vue is a **progressive framework**, that means allow us to write an scalable web application. So we can begin writing an small project like a landing page, using a very tiny javascript library skiping huge modules or features that we are not going to use until more advances phases of our project. Then, as soon as our requirements turns more complex, we could add those modules to reach our goals.

Vue like the DOM works in an tree manner over the HTML. Starting from a `root` component, in our case `<div id="app">`, this means that everything that is out of `root`, is not reachable by Vue. Which is really useful, since we can integrate a Vue application in any web application that is already using other technology, such as React, jQuery or even plain javascript.
