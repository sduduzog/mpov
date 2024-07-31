---
# You can also start simply with 'default'
# https://talks.antfu.me/2024/vue-amsterdam/presenter/1 talk research
theme: apple-basic
title: My Point of Vue
mdc: true
layout: intro-image-right
image: /i_agree.png
---

## <v-click>Hello</v-click>

<v-clicks>

- Authoring components
- Nuxt & Nitro
- 3rd party Integrations
- and one more thing...

</v-clicks>

# My point of <span class="text-[#41B883]" v-mark="{color: '#41B883'}">Vue</span>


<!--
[click] Hello everyone.

I'm really excited to be here.

Today I'll talk about [click] the many ways of writing a component in vue, [click] nuxt and nitro, the actual write once, deploy everywhere frameworks, [click] touch on some useful integrations and other tools in the ecosystem and [click] finally, if I still have some time, I'll tell you about sli.dev

At the end or this talk, I hope to have added one or two new items into your toolbox and re-enabled you to look at web development from 

[click] my point of view.
-->

---
layout: section
---

# <span v-mark.circle.teal>Sdu</span>duzo Gumede

- Consultant at Daemon

- Co-host of the ZATechRadio podcast
<div class="flex items-center gap-2"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 14 14"><g fill="none"><g clip-path="url(#primeTwitter0)"><path fill="currentColor" d="M11.025.656h2.147L8.482 6.03L14 13.344H9.68L6.294 8.909l-3.87 4.435H.275l5.016-5.75L0 .657h4.43L7.486 4.71zm-.755 11.4h1.19L3.78 1.877H2.504z"/></g><defs><clipPath id="primeTwitter0"><path fill="#fff" d="M0 0h14v14H0z"/></clipPath></defs></g></svg><span>@sduduzo_g</span></div>

<v-click>
<Tweet id="1790664621507920214" />
</v-click>


<!--
First let me introduce myself. My name is Sduduzo Gumede, [click] or Sdu, for short

I'm a consultant at Daemon, a consultancy based in the UK,

I'm one-3rd of the ZATechRadio podcast,

a father to a beautiful little girl
[click] and a serial tweeter of note.

Do follow me for what could either be, great words of coding wizdom or dad jokes that should have remained in drafts 

--> 

---
layout: center
---

<div class="flex h-16 justify-evenly items-center">
  <img src="/codeo-logo.png" v-mark.bracket class="object-contain h-full" />
  <img src="/yumbi-logo.png" v-mark.circle class="object-contain h-full w-80" />
</div>

<div class="flex gap-8 mt-20 h-16 justify-evenly items-center">
  <img v-click src="/aspnet.jpg" class="object-contain h-full" />
  <img v-click src="/vue.jpg" class="object-contain h-full" />
  <img v-click src="/angular.jpg" v-mark.crossed-off class="object-contain h-full" />
  <img v-click src="/angularjs.png" class="object-contain h-full" />
</div>

<!--
Before joining Daemon, I worked for a consultancy based in Durban called [click] Codeo and  [click] I was primarily focused on the Yumbi platform.
The main stack was [click] asp.net, [click] VueJS, [click] and God forbid angular.js, [click] the first one.
-->

---
layout: two-cols
class: grid items-center 
---

<div v-click>
  <img src="/8yocso.jpg" />
</div>


::right::

<div class="grid grid-cols-3 items-center">
  <img src="/tab-steers.png" />
  <img src="/tab-debonairs.png" />
  <img src="/tab-fishaways.png" />
</div>


<!--
So the front-end framework chosen to power callcenters and online ordering platforms, in 18 different countries and thousands of restaurants. [click] VueJS was unleashed as the perfect fit.
-->
---
layout: bullets
---

# Vuejs is approachable

<!--
It's ridiculously easy to pick up, and learn whether you're new to web frameworks, or coming from an alternative one. It would take most people hours to days to get up to speed and feel productive in a team
-->

---
layout: bullets
---

# Vuejs is scalable

<v-clicks>

- Versatility
- Maintainability
- Customisability
- Modularity

</v-clicks>

<!--
We were able to use VueJS as tiny patches of user interfaces in legacy applications that power the back-office for franchisees, support and brand marketers to progressively enhance their experience and also as a full featured framework that we've all at least used once to order a pizza or a burger before  

[click] Continuing with the ordering system as an example, we were able to introduce and adopt an architecture, on top of the framework that made it easy for engineers from object-oriented programming backgrounds and back-end developers to contribute meaningfully. It also makes working with designers with no interests in javascript, particularly easy too, thanks to vue templates

[click] Being able to come in, as a new developer on the team, and introduce meaningful work was testament of how a well architected Vue project is easy to maintain, no matter how large it had become

[click] Our Vue project was successfully extended through webpack to support multiple brands and designs while using the same codebase for the business logic

[click] Not only does the logic written, serve the web application, but using the react native bridge for the mobile apps, the same VueJS project leverages some native features you find either on Android or iOS to refine the end user's experience of the platform, for example better location detection using the devices GPS, and tailored push notifications. Think debonairs birthday vouchers
-->

---
layout: center
---

<div v-click>
  <img src="/8yomoa.jpg" />
</div>

<!--
TLDR; I've built buttons in Vuejs being pressed in 18 different countries, and counting. Which is pretty cool

[click] If you've been waiting to see some code. I believe I've done the least exiting part of this talk.

Let's look at the basic building block of a Vue app
-->

---
layout: two-cols-header
---

# Single-File Components

<!--
From the first time I touched VueJS to learn it, to using it in production, VueJS has undergone a single major version update. From version 2 to version 3. And throughout, defining a component remained fairly the same.
-->
---
layout: two-cols-header
---

# Single-File Components

::left::

Options API

````md magic-move
```vue {all|1-3|5-13|15-19|all|none}
<template>
  <button @click="count++">Count is: {{ count }}</button>
</template>

<script>
export default {
  data() {
    return {
      count: 0
    }
  }
}
</script>

<style>
button {
  font-weight: bold;
}
</style>
```

```vue {none|none}
<template>
  <button @click="count++">Count is: {{ count }}</button>
</template>

<script>
export default {
  data() {
    return {
      count: 0
    }
  }
}
</script>

<style>
button {
  font-weight: bold;
}
</style>
```

```vue
<template>
  <button @click="count++">Count is: {{ count }}</button>
</template>

<script>
export default {
  data() {
    return {
      count: 0
    }
  }
}
</script>
```

```vue {12-16|8-10,13-15}
<template>
  <button @click="count++">Count is: {{ count }}</button>
</template>

<script>
export default {
  data() {
    return {
      count: 0
    }
  },
  computed: {
    doubled() {
      return this.count * this.count
    }
  }
}
</script>
```
````
::right::

Composition API

````md magic-move {at:1}
```vue {all|1-3|5-15|17-21|all|5-15}
<template>
  <button @click="count++">Count is: {{ count }}</button>
</template>

<script>
import { ref } from 'vue'

export default {
  setup() {
    const count = ref(0)

    return { count }
  }
}
</script>

<style>
button {
  font-weight: bold;
}
</style>
```

```vue {5|5-8}
<template>
  <button @click="count++">Count is: {{ count }}</button>
</template>

<script setup>
import { ref } from 'vue'
const count = ref(0)
</script>

<style>
button {
  font-weight: bold;
}
</style>
```


```vue {none}
<template>
  <button @click="count++">Count is: {{ count }}</button>
</template>

<script setup>
import { ref } from 'vue'
const count = ref(0)
</script>
```

```vue {8|8}
<template>
  <button @click="count++">Count is: {{ count }}</button>
</template>

<script setup>
import { ref, computed } from 'vue'
const count = ref(0)
const doubled computed(() => count.value * 2)
</script>
```
````
<style>
  .two-cols-header {
    @apply gap-1;
  }
</style>

<!--
Single file components are still rocking the iconic trio. The [click] template, [click] script and [click] style blocks [click] encapsulating and colocating the view, logic and styling of a component in the same file.

[click] The vue team also introduced the composition api, a way to define your logic with imported API functions, along with it, [click] the setup attribute, [click] which hints Vue to make compile-time transforms allowing us to compose our logic with less boilerplate.

[click] Alternatively, you can still use the Options API, [click] implemented on top of the composition api, but still centered around the concept of a "component instance" [click] (this) which aligns better with a class-based mental model. This also makes the Options API beginner friendly, but both interfaces are powered by the same underlying system.

Speaking of class-based mental models
-->

---

# Class based components

<div class="flex gap-4" v-click.hide="'+1'">
<span v-click v-mark.crossed-off>vue-class-component</span>
<span v-click="'+0'" v-mark.crossed-off>vue-property-decorator</span>
<span v-click>vue-facing-decorator</span>
</div>

<v-click at="+0">

````md magic-move
```vue {all|7}
<template>
  <button @click="count++">Count is: {{ count }}</button>
</template>

<script lang="ts">
class Counter {
  count = 0
}
</script>

```

```vue {9-11}
<template>
  <button @click="count++">Count is: {{ count }}</button>
</template>

<script lang="ts">
class Counter {
  count = 0

  mounted() {
    console.log(this.count)
  }
}
</script>
```

```vue {13-15}
<template>
  <button @click="count++">Count is: {{ count }}</button>
</template>

<script lang="ts">
class Counter {
  count = 0

  mounted() {
    console.log(this.count)
  }

  get doubled() {
    return this.count * 2
  }
}
</script>
```

```vue {6,8}
<template>
  <button @click="count++">Count is: {{ count }}</button>
</template>

<script lang="ts">
import { Vue } from 'vue-facing-decorator'

class Counter extends Vue {
  count = 0

  mounted() {
    console.log(this.count)
  }

  get doubled() {
    return this.count * 2
  }
}
</script>

```
```vue {6,8,21}
<template>
  <button @click="count++">Count is: {{ count }}</button>
</template>

<script lang="ts">
import { Component, Vue, toNative } from 'vue-facing-decorator'

@Component
class Counter extends Vue {
  count = 0

  mounted() {
    console.log(this.count)
  }

  get doubled() {
    return this.count * 2
  }
}

export default toNative(Counter)
</script>

```

```vue
<template>
  <button @click="count++">Count is: {{ count }}</button>
</template>

<script lang="ts">
import { Component, Vue, toNative } from 'vue-facing-decorator'

@Component
class Counter extends Vue {
  count = 0

  mounted() {
    console.log(this.count)
  }

  get doubled() {
    return this.count * 2
  }
}

export default toNative(Counter)
</script>

```
````

</v-click>

<style>
  .two-cols-header {
    @apply gap-1;
  }
</style>

<!--
You can also define vue components as javascript classes. [click] Of course with some library help. You would use vue-class-component as the decorator for your component definition, and 
vue-property-decorator that builds on top of the latter to add more decorators for your component characteristics, like props, and emits

[click] I should mention, it's no longer recommended to use class-based components in Vue 3. Even the libraries that enabled this are now deprecatd in favour of the available functional approaches to component definitions.

[click] But if you really want to continue with this direction, folks in the vue community created vue-facing-decorator which re-enables class based components with extra flavour added by Vue 3 

[click] If you know how to write a pure javascript class, you pretty much know how to write a class based component. 

[click] A class property will be your data property of course [click] lifecycle hooks are just regular methods of the class [click] getters enable you to define computed properties

[click] Of course this is a vue component, so you class should extend vue, [click] we then decorate it as a component and finally, use the utility toNative that transforms your class into a native vue options API component.

[click] Throughout these different ways of composing our component logic, the template and styles can remain the same
-->

---
layout: quote
---

# "Yea but v-for and v-if are just weird"
an indenial react dev

<!--
Now there's a subset of devs that see the Vue template syntax and think "Yea but v-for and v-if are just weird" I have two questions then.

1. Do you also think other html attributes are werid? Because honestly, vue templates feel almost native to HTML, which was the intended purpose
-->

---
layout: section
---

```tsx {all|3,6}
function TestPage() {
  return (
    <>
      <h1 className="">About</h1>
      <p>Hello, world!</p>
    </>
  )
}
```

<h1 v-after>???</h1>

<!--
Second question for people using jsx and/or tsx [click] 2. What are those? 
-->

---
layout: center
---

<v-click>

![lewis looking at jsx pills](/8ysoiz.jpg)

</v-click>

<!--
It does happen though in some instances within a vue project, [click] you get use cases for jsx, whether you're trying out vue and you still want to define your user interfaces with something familiar or you need the flexibility of being able to define multiple functional components in a single file.
-->

---
layout: two-cols
---

## Counter.vue

```vue
<template>
  <button @click="count++">Count is: {{ count }}</button>
</template>

<script>
import { ref } from 'vue'

export default {
  setup() {
    const count = ref(0)

    return { count }
  }
}
</script>
```

::right::

## Counter.jsx

```tsx
import { ref } from 'vue'

export default {
  setup() {
    const count = ref(0)

    return () => (
      <button onClick={() => count.value++}>
        Count is: {{ count.value }}
      </button>
    )
  }
}
```


<style>
  .two-columns {
    @apply gap-1;
  }
</style>

<!--
Using our previous composition api example, we can pretty much rewrite every component we want as jsx. 

But be careful when coming from react as some things won't be particularly the same.
- in Vue JSX for instance, you can use html attributes such as class and for in form labels, which you can't in react
-->

---

# Templates vs. Render Functions

<v-click>

````md magic-move
```vue {all|7}
<script setup >
import { ref } from 'vue';

const count = ref(0)
</script>
<template>
  <h1>Hello, world</h1>
  <button>{{ count }}</button>
</template>
```

```js {19|all}
import { ref } from 'vue';

const __sfc__ = {
  __name: 'App',
  setup(__props, { expose: __expose }) {
  __expose();

const count = ref(0)

const __returned__ = { count, ref }
Object.defineProperty(__returned__, '__isScriptSetup', { enumerable: false, value: true })
return __returned__
}

};
import { createElementVNode as _createElementVNode, toDisplayString as _toDisplayString,
  Fragment as _Fragment, openBlock as _openBlock, createElementBlock as _createElementBlock } from "vue"

const _hoisted_1 = /*#__PURE__*/_createElementVNode("h1", null, "Hello, world", -1 /* HOISTED */)
function render(_ctx, _cache, $props, $setup, $data, $options) {
  return (_openBlock(), _createElementBlock(_Fragment, null, [
    _hoisted_1,
    _createElementVNode("button", null, _toDisplayString($setup.count), 1 /* TEXT */)
  ], 64 /* STABLE_FRAGMENT */))
}
__sfc__.render = render
__sfc__.__file = "src/App.vue"
export default __sfc__
```
````
</v-click>

<!--
Fun fact!

Vue templates are compiled into render functions.

And jsx in Vue is just a fancy render function

So why does Vue recommend we  use templates?

[click]

- Templatesa are closer to actual html, so if you know how to work with html, you know how to work with vue templates

- Templates are easier to statically analyze due to their deterministric syntax. The vue compiler is way better at writing efficient and performant render functions than you and I could ever

[click] During compilation, parts of a template that don't contain dynamic bindings [click] will be hoisted and reused on every re-render

[click] The compiler can statically analyze the template and leave hints in the generated code so that the runtime can take shortcuts whenever possible
-->

---
layout: section
---

<v-clicks>

- Routing
- State management
- SEO & Meta tags
- Data fetching
- So much more, etc etc

</v-clicks>

<v-switch :at="1">
  <template #0-6><h1>So whats next?</h1></template>
  <template #6><h1 class="flex items-center">So whats
<svg v-click.after xmlns="http://www.w3.org/2000/svg" class="ml-4 mb-1" width="180" height="70" viewBox="0 0 128 32" fill="none">
<path d="M60.32 32C60.6656 32 60.96 31.7135 60.96 31.36V16.48C60.96 16.48 61.76 17.92 63.2 20.32L69.44 31.04C69.7255 31.6384 70.359 32 70.88 32H75.2V8H70.88C70.5923 8 70.24 8.23906 70.24 8.64V23.68L67.36 18.56L61.6 8.8C61.3197 8.3026 60.7166 8 60.16 8H56V32H60.32Z" fill="black"/>
<path d="M116.16 14.72H118.24C118.77 14.72 119.2 14.2902 119.2 13.76V9.6H123.68V14.72H128V18.56H123.68V25.44C123.68 27.12 124.489 27.84 125.92 27.84H128V32H125.28C121.592 32 119.2 29.6114 119.2 25.6V18.56H116.16V14.72Z" fill="black"/>
<path d="M94.56 14.72V24.64C94.56 26.8806 93.7188 28.7695 92.48 30.08C91.2412 31.3905 89.5306 32 87.2 32C84.8694 32 82.9988 31.3905 81.76 30.08C80.5422 28.7695 79.68 26.8806 79.68 24.64V14.72H82.24C82.7859 14.72 83.3231 14.8195 83.68 15.2C84.0369 15.5593 84.16 15.7704 84.16 16.32V24.64C84.16 25.9294 84.2331 26.7259 84.8 27.36C85.3669 27.973 86.0662 28.16 87.2 28.16C88.3548 28.16 88.8731 27.973 89.44 27.36C90.0069 26.7259 90.08 25.9294 90.08 24.64V16.32C90.08 15.7704 90.2031 15.4205 90.56 15.04C90.8736 14.7057 91.2045 14.7136 91.68 14.72C91.7457 14.7209 91.9337 14.72 92 14.72H94.56Z" fill="black"/>
<path d="M108.16 23.04L113.6 14.72H109.44C108.916 14.72 108.45 14.9081 108.16 15.36L105.6 19.2L103.2 15.52C102.91 15.0681 102.284 14.72 101.76 14.72H97.76L103.2 22.88L97.28 32H101.44C101.96 32 102.429 31.486 102.72 31.04L105.6 26.72L108.64 31.2C108.931 31.646 109.4 32 109.92 32H114.08L108.16 23.04Z" fill="black"/>
<path d="M26.88 32H44.64C45.2068 32.0001 45.7492 31.8009 46.24 31.52C46.7308 31.2391 47.2367 30.8865 47.52 30.4C47.8033 29.9135 48.0002 29.3615 48 28.7998C47.9998 28.2381 47.8037 27.6864 47.52 27.2001L35.52 6.56C35.2368 6.0736 34.8907 5.72084 34.4 5.44C33.9093 5.15916 33.2066 4.96 32.64 4.96C32.0734 4.96 31.5307 5.15916 31.04 5.44C30.5493 5.72084 30.2032 6.0736 29.92 6.56L26.88 11.84L20.8 1.59962C20.5165 1.11326 20.1708 0.600786 19.68 0.32C19.1892 0.0392139 18.6467 0 18.08 0C17.5133 0 16.9708 0.0392139 16.48 0.32C15.9892 0.600786 15.4835 1.11326 15.2 1.59962L0.32 27.2001C0.0363166 27.6864 0.000246899 28.2381 3.05588e-07 28.7998C-0.000246288 29.3615 0.0367437 29.9134 0.32 30.3999C0.603256 30.8864 1.10919 31.2391 1.6 31.52C2.09081 31.8009 2.63324 32.0001 3.2 32H14.4C18.8379 32 22.068 30.0092 24.32 26.24L29.76 16.8L32.64 11.84L41.44 26.88H29.76L26.88 32ZM14.24 26.88H6.4L18.08 6.72L24 16.8L20.0786 23.636C18.5831 26.0816 16.878 26.88 14.24 26.88Z" fill="#00DC82"/>
</svg>
?</h1></template>
</v-switch>


<!--
topics

Nuxt and Nitro: "Write once, deploy everywhere"
3rd party integrations (i.e. embedding a graphql server)
unjs packages and production use cases
Discover sli.dev

-->

<!--
Okay, now that you're a professional at writing vue components and you're building the next facebook

[click] Do you configure vue-router for navigation?

[click] Do you setup pinia for state management because it's better than vuex?

[click] Do you fight with server side rendering, and fiddle through npm to find libraries to help with SEO and meta tags?

[click] Or perhaps add that blazing fast data fetching library?

[click] There's actually a lot of moving pieces to bring together when building a project for the real world that we need to consider. So what's nuxt

[click] Well its a batteries-included framework for building performant and production-grade full-stack web apps and websites
-->

---
layout: two-cols
---

<h1 class="flex items-center">
<svg xmlns="http://www.w3.org/2000/svg" class="" width="180" height="180" viewBox="0 0 128 32" fill="none">
<path d="M60.32 32C60.6656 32 60.96 31.7135 60.96 31.36V16.48C60.96 16.48 61.76 17.92 63.2 20.32L69.44 31.04C69.7255 31.6384 70.359 32 70.88 32H75.2V8H70.88C70.5923 8 70.24 8.23906 70.24 8.64V23.68L67.36 18.56L61.6 8.8C61.3197 8.3026 60.7166 8 60.16 8H56V32H60.32Z" fill="black"/>
<path d="M116.16 14.72H118.24C118.77 14.72 119.2 14.2902 119.2 13.76V9.6H123.68V14.72H128V18.56H123.68V25.44C123.68 27.12 124.489 27.84 125.92 27.84H128V32H125.28C121.592 32 119.2 29.6114 119.2 25.6V18.56H116.16V14.72Z" fill="black"/>
<path d="M94.56 14.72V24.64C94.56 26.8806 93.7188 28.7695 92.48 30.08C91.2412 31.3905 89.5306 32 87.2 32C84.8694 32 82.9988 31.3905 81.76 30.08C80.5422 28.7695 79.68 26.8806 79.68 24.64V14.72H82.24C82.7859 14.72 83.3231 14.8195 83.68 15.2C84.0369 15.5593 84.16 15.7704 84.16 16.32V24.64C84.16 25.9294 84.2331 26.7259 84.8 27.36C85.3669 27.973 86.0662 28.16 87.2 28.16C88.3548 28.16 88.8731 27.973 89.44 27.36C90.0069 26.7259 90.08 25.9294 90.08 24.64V16.32C90.08 15.7704 90.2031 15.4205 90.56 15.04C90.8736 14.7057 91.2045 14.7136 91.68 14.72C91.7457 14.7209 91.9337 14.72 92 14.72H94.56Z" fill="black"/>
<path d="M108.16 23.04L113.6 14.72H109.44C108.916 14.72 108.45 14.9081 108.16 15.36L105.6 19.2L103.2 15.52C102.91 15.0681 102.284 14.72 101.76 14.72H97.76L103.2 22.88L97.28 32H101.44C101.96 32 102.429 31.486 102.72 31.04L105.6 26.72L108.64 31.2C108.931 31.646 109.4 32 109.92 32H114.08L108.16 23.04Z" fill="black"/>
<path d="M26.88 32H44.64C45.2068 32.0001 45.7492 31.8009 46.24 31.52C46.7308 31.2391 47.2367 30.8865 47.52 30.4C47.8033 29.9135 48.0002 29.3615 48 28.7998C47.9998 28.2381 47.8037 27.6864 47.52 27.2001L35.52 6.56C35.2368 6.0736 34.8907 5.72084 34.4 5.44C33.9093 5.15916 33.2066 4.96 32.64 4.96C32.0734 4.96 31.5307 5.15916 31.04 5.44C30.5493 5.72084 30.2032 6.0736 29.92 6.56L26.88 11.84L20.8 1.59962C20.5165 1.11326 20.1708 0.600786 19.68 0.32C19.1892 0.0392139 18.6467 0 18.08 0C17.5133 0 16.9708 0.0392139 16.48 0.32C15.9892 0.600786 15.4835 1.11326 15.2 1.59962L0.32 27.2001C0.0363166 27.6864 0.000246899 28.2381 3.05588e-07 28.7998C-0.000246288 29.3615 0.0367437 29.9134 0.32 30.3999C0.603256 30.8864 1.10919 31.2391 1.6 31.52C2.09081 31.8009 2.63324 32.0001 3.2 32H14.4C18.8379 32 22.068 30.0092 24.32 26.24L29.76 16.8L32.64 11.84L41.44 26.88H29.76L26.88 32ZM14.24 26.88H6.4L18.08 6.72L24 16.8L20.0786 23.636C18.5831 26.0816 16.878 26.88 14.24 26.88Z" fill="#00DC82"/>
</svg>
</h1>

::right::

<v-switch>
  <template #1>
    <img src="/remix-light.png"  class="w-96"/>
  </template>

  <template #2>
    <img src="/remix_aqcuired.png"  class=""/>
  </template>

  <template #3>
    <img src="/Gatsby_Logo.png"  class="p-10"/>
  </template>

  <template #4>
    <img src="/gatsby_aqcuired.png"  class=""/>
  </template>

  <template #5>
    <img src="/nextjs-logo-square.webp"  class="h-50 w-full object-contain"/>
  </template>

  <template #6>
    <img src="/now_config.png"  class="w-full"/>
  </template>
</v-switch>

<style>
  .col-right {
    @apply col-span-2
  }
</style>

<!--
Nuxt is a Vue meta framework as much as next, remix and gatsby are react meta frameworks. 

But there are subtle details that set these frameworks apart, even with all the similarities

[click] Nuxt and remix both focus on fast user experiences and efficient data handling. By the way, remix was, for a brief moment, only available through a paid license called "supporter preview" to developers, about a year later, remix was made open source under the MIT license. [click] Almost a year after that, it was aqcuired by shopify

[click] Gatsby started as a blazing-fast static site generator for React, then from version two and up, they started introducing more interactive features, like server side rendering, integrations with CMS systems and GraphQL. Nuxt not only has had first class support for static site generation but the plugin system allowed developers to bring in their favourite libraries to the framework. [click] By the way Gatsby is not dead or discontinued, it has been aqcuired by netlify 

[click] Nuxt and next share a little more than the latter comparisons, for one, nuxt was inspired greatly by next.js, from the name to the feature-rich meta framework that it is today. Back when vercel was called zeit, next eventually added support for api event handlers, which when deploying to zeit, would become serverless functions for your application. [click] To achieve the same for nuxt, you had to add a custom configuration pointing to a folder holding express.js handlers, and for local development, you would create a nuxt plugin that uses express.js for these handlers, which wasn't great for developer experience
-->

---
layout: center
---

<img src="/i_agree.png" class="object-contain w-full h-96"/>

<!--
Now this is not to say, what framework is better than the other. We all have different preferences and there's always going to be a better tool for any web development job, apart from the ones we choose as our favourites. What I've grown to appreciate with web development over the years is how teachings from one ecosystem translate well to another.

If you don't take into account, the nuances brought on by the syntax used to define user interfaces, all these frameworks are fundamentally the same. The design patterns they follow are the same, the APIs they are introducing now are the same. Think hooks, for react, vue, and solidjs, or signals for again vue, svelte and solidjs
-->

---
layout: two-cols
---

![poking with a stick meme](/8yomoa.jpg)

<!--
If there's anyone wondering how a nuxt project looks like, we'll now go over enough details to give you an idea but not too indepth that it becomes boring
-->

---
layout: two-cols-header
---

<h1 class="flex items-center">
<svg xmlns="http://www.w3.org/2000/svg" class="" width="180" height="180" viewBox="0 0 128 32" fill="none">
<path d="M60.32 32C60.6656 32 60.96 31.7135 60.96 31.36V16.48C60.96 16.48 61.76 17.92 63.2 20.32L69.44 31.04C69.7255 31.6384 70.359 32 70.88 32H75.2V8H70.88C70.5923 8 70.24 8.23906 70.24 8.64V23.68L67.36 18.56L61.6 8.8C61.3197 8.3026 60.7166 8 60.16 8H56V32H60.32Z" fill="black"/>
<path d="M116.16 14.72H118.24C118.77 14.72 119.2 14.2902 119.2 13.76V9.6H123.68V14.72H128V18.56H123.68V25.44C123.68 27.12 124.489 27.84 125.92 27.84H128V32H125.28C121.592 32 119.2 29.6114 119.2 25.6V18.56H116.16V14.72Z" fill="black"/>
<path d="M94.56 14.72V24.64C94.56 26.8806 93.7188 28.7695 92.48 30.08C91.2412 31.3905 89.5306 32 87.2 32C84.8694 32 82.9988 31.3905 81.76 30.08C80.5422 28.7695 79.68 26.8806 79.68 24.64V14.72H82.24C82.7859 14.72 83.3231 14.8195 83.68 15.2C84.0369 15.5593 84.16 15.7704 84.16 16.32V24.64C84.16 25.9294 84.2331 26.7259 84.8 27.36C85.3669 27.973 86.0662 28.16 87.2 28.16C88.3548 28.16 88.8731 27.973 89.44 27.36C90.0069 26.7259 90.08 25.9294 90.08 24.64V16.32C90.08 15.7704 90.2031 15.4205 90.56 15.04C90.8736 14.7057 91.2045 14.7136 91.68 14.72C91.7457 14.7209 91.9337 14.72 92 14.72H94.56Z" fill="black"/>
<path d="M108.16 23.04L113.6 14.72H109.44C108.916 14.72 108.45 14.9081 108.16 15.36L105.6 19.2L103.2 15.52C102.91 15.0681 102.284 14.72 101.76 14.72H97.76L103.2 22.88L97.28 32H101.44C101.96 32 102.429 31.486 102.72 31.04L105.6 26.72L108.64 31.2C108.931 31.646 109.4 32 109.92 32H114.08L108.16 23.04Z" fill="black"/>
<path d="M26.88 32H44.64C45.2068 32.0001 45.7492 31.8009 46.24 31.52C46.7308 31.2391 47.2367 30.8865 47.52 30.4C47.8033 29.9135 48.0002 29.3615 48 28.7998C47.9998 28.2381 47.8037 27.6864 47.52 27.2001L35.52 6.56C35.2368 6.0736 34.8907 5.72084 34.4 5.44C33.9093 5.15916 33.2066 4.96 32.64 4.96C32.0734 4.96 31.5307 5.15916 31.04 5.44C30.5493 5.72084 30.2032 6.0736 29.92 6.56L26.88 11.84L20.8 1.59962C20.5165 1.11326 20.1708 0.600786 19.68 0.32C19.1892 0.0392139 18.6467 0 18.08 0C17.5133 0 16.9708 0.0392139 16.48 0.32C15.9892 0.600786 15.4835 1.11326 15.2 1.59962L0.32 27.2001C0.0363166 27.6864 0.000246899 28.2381 3.05588e-07 28.7998C-0.000246288 29.3615 0.0367437 29.9134 0.32 30.3999C0.603256 30.8864 1.10919 31.2391 1.6 31.52C2.09081 31.8009 2.63324 32.0001 3.2 32H14.4C18.8379 32 22.068 30.0092 24.32 26.24L29.76 16.8L32.64 11.84L41.44 26.88H29.76L26.88 32ZM14.24 26.88H6.4L18.08 6.72L24 16.8L20.0786 23.636C18.5831 26.0816 16.878 26.88 14.24 26.88Z" fill="#00DC82"/>
</svg>
</h1>

::left::

````md magic-move
```md {all|4|4|3|2}
.
├── app.vue
├── nuxt.config.js
└── package.json
```

```md {2-3}
.
├── pages/
│   └── index.tsx
├── app.vue
├── nuxt.config.js
└── package.json
```

```md {4-5}
.
├── pages/
│   ├── index.tsx
│   └── users-[group]/
│       └── [id].vue
├── app.vue
├── nuxt.config.js
└── package.json
```
```md {6-9}
.
├── pages/
│   ├── index.tsx
│   └── users-[group]/
│       └── [id].vue
├── server/
│   └── api/
│       ├── hello.ts
│       └── test.post.ts
├── app.vue
├── nuxt.config.js
└── package.json
```

````

::right::

<v-click :at="1">
````md magic-move {at:2}
```json {all|6,9}
{
  "name": "nuxt-app",
  "private": true,
  "type": "module",
  "scripts": {
    "dev": "nuxt dev",
  },
  "devDependencies": {
    "nuxt": "^3.12.4",
  }
}
```

```ts
export default defineNuxtConfig({
  // my nuxt config
})
```
```vue
<template>
  <h1>Hello World!</h1>
</template>
```
```tsx
export default defineComponent({
  render () {
    return <h1>Index page</h1>
  }
})
// .vue, .js, .jsx, .mjs, .ts or .tsx supported
```

```vue
<template>
  <p>{{ $route.params.group }} {{ $route.params.id }}</p>
</template>
```
```ts
export default defineEventHandler((event) => {
  return {
    hello: 'world'
  }
})
```
````

</v-click>


<style>
  .two-cols-header {
    @apply gap-1
  }
</style>

<!--
What's been the most important aspect of meta frameworks is the folder structure. Nuxt uses this fact a lot to its advantage, the key to being comfortable with nuxt is to use and appreciate this too.

You need at least 3 files to have a running nuxt project

[click] the package.json file [click] to specify dependencies and npm scripts to start your dev server

[click] the nuxt config file

[click] lastly, the main component of your Nuxt application. 

[click] The pages directory is optional. And usually added as your project grows. Its supports a bunch of extensions out of the box, so you can define your components however you like, including the class-based components that we mentioned earlier

[click] Dynamic routes are also denoted using the file names for your pages. You use square brackets to denote the dynamic segment of your route.

If you're using typescript, these parameters will be fully typed when accessing them within your component

[click] My favourite part of working with nuxt is adding api endpoints. It's as simple as adding handlers in the server api folder. Of all features I was looking for when nuxt version 3 was released in 2021, was being able to add backend code without the need to integrate express.js or similar libraries as we had to in the past
-->
