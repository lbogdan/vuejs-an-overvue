## Agenda

- A Bit of History
- Core Concepts
- Ecosystem
- Live Coding: Vue CLI & Vue 2
- Vue.js 3 Highlights
- Live Coding: Vite & Vue 3


## A Bit of History

> "For me, Angular offered something cool which is data binding and a data driven way of dealing with a DOM, so you don’t have to touch the DOM yourself. [...] I figured, what if I could just extract the part that I really liked about Angular and build something really lightweight without all the extra concepts involved? [...] I started this experiment just trying to replicate this minimal feature set, like declarative data binding. That was basically how Vue started."

[Evan You, Vue.js creator](https://www.freecodecamp.org/news/between-the-wires-an-interview-with-vue-js-creator-evan-you-e383cbf57cc4/)


## A Bit of History (cont.)

> "Current React learning status: overwhelmed. Learning @vuejs because it looks easy and has pretty website. 👍"

[Taylor Otwell, Laravel (PHP framework) creator](https://twitter.com/taylorotwell/status/590281695581982720)


## A Bit of History (cont.)

- [version history](https://en.wikipedia.org/wiki/Vue.js#History)
- stable API
- few breaking changes between major versions
- migration guides & tools


## "The Progressive JavaScript Framework"

- start small, get as complex as you want

![The Progressive JavaScript Framework](https://sites.google.com/site/webdevelopart/_/rsrc/1511099898084/22-script/javascript/vue-js/Progressive%20framework.png)

[Evan You, Vue js the Progressive Framework](https://www.youtube.com/watch?v=pBBSp_iIiVM)


## Components
- self-contained UI units
- single file components (SFC): one component per `.vue` file
- `<template>` + `<script>` (+ `<style>`)
- "just" HTML, JavaScript, CSS
- can also use JSX, TypeScript, SCSS etc.
- needs a bundler (Vue CLI)


## Components: example
```html
<template>
  <section>
    <img :src="profilePictureUrl" alt="Profile Picture">
    <div>{{ fullName }}</div>
  </section>
</template>

<script>
export default {
  name: 'User',
  data() {
    return {
      firstName: 'Bogdan',
      lastName: 'Luca',
      profilePictureUrl: 'https://jsheroes.io/static/img/2020/speakers/bogdan-luca.jpg',
    };
  },
  computed: {
    fullName() {
      return `${this.firstName} ${this.lastName}`;
    },
  },
}
</script>

<style scoped>
img {
  width: 100px;
}
section {
  font-weight: bold;
}
</style>
```

## Declarative vs. Imperative
- define how a component looks like (markup) as a function of state vs. tell it step-by-step how to get there
- don't worry about DOM manipulation, focus on data manipulation


## Component State
- internal, returned from `data()`
- derived, through `computed`
- external, through `props`


## Reactivity
- implicit, through assignment & mutating array methods
- Vue.js 2: uses ES5 getters & setters, but there's gotchas:
  - `obj.newProperty = value;`
  - `arr[index] = value;`
- Vue.js 3: uses ES6 Proxy
- [data dependency tracking](https://vuejs.org/v2/guide/reactivity.html#How-Changes-Are-Tracked)
- vs. React - explicit reactivity - need to explicitly call the setter
- vs. Angular - change detection using zones - very inefficient by default, needs manual fine-tuning


## Vue.js Ecosystem
- [Vue CLI](https://cli.vuejs.org/) - Standard Tooling for Vue.js Development
- [vue-router](https://router.vuejs.org/) - Single Page App (SPA) routing
- [vuex](https://vuex.vuejs.org/) - global state management
- [vue-test-utils](https://vue-test-utils.vuejs.org/) - unit testing utility library
- [Vetur](https://marketplace.visualstudio.com/items?itemName=octref.vetur) - VSCode extension to support SFCs
- [Vue.js devtools](https://chrome.google.com/webstore/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd)
- NuxtJS, VuePress, Gridsome - frameworks on top of Vue.js (SSR, static)
- [Awesome Vue.js - A curated list of awesome things related to Vue.js](https://github.com/vuejs/awesome-vue)
- community
  - [forum](https://forum.vuejs.org/)
  - [Discord chat](https://chat.vuejs.org/) (I'm `BogdanL` there)


## Vue CLI
- plugin based
- out-of-the-box: Babel, TypeScript, Progressive Web App (PWA), ESLint, unit testing - Mocha + Chai, Jest, end-to-end (E2E) testing - Cypress, Nightwatch, WebdriverIO
- 3rd party: Electron, Apollo (GraphQL), Storybook etc.


## Live Coding Time!

Vue CLI & Simple To-Do App


## Vue.js 3 Highlights

- recently released - 18 September
- Composition API ([vs. Options API](https://user-images.githubusercontent.com/499550/62783026-810e6180-ba89-11e9-8774-e7771c8095d6.png))
  - better TypeScript support
- improved reactivity - uses Proxy instead of getters / setters; no IE11 support
- [Portal (Teleport)](https://v3.vuejs.org/guide/teleport.html) added in core
- supports multiple root nodes (finally!)
- Suspense (beta) - async components
- [Vite](https://github.com/vitejs/vite) - Vue CLI alternative, uses browser native ES Module imports, much faster!
- the ecosystem is lagging behind, but it's slowly getting there!


## Live Coding Time, Take Two!

Vite & Refactoring to Composition API


## Q & A

Ask Away!


## Thank You!

🙏


##
