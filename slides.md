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

<div class="absolute top-10">
  <span class="font-700">
    Sdu Gumede
  </span>
</div>

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
<Tweet id="1798338369698812340" />
</v-click>


<!--
My name is Sduduzo Gumede, [click] or Sdu, for short

I'm a consultant at Daemon,
a co-host of the ZATechRadio podcast,
[click] and a serial tweeter of note

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
The main stack was [click] DOTNET, [click] VueJS, [click] and God forbid angular.js, [click] the first one.
 
-->

---

<!--
VueJS powers one of the bigest restaurant ordering platforms in Africa. And it was and still is the perfect choice for such a platform.

- It's ridiculously easy to pick up, and learn whether you're new to web frameworks, or coming from an alternative one
- It makes working with designers with no interests in javascript, particularly easy too, thanks to vue templates
- it's very scalable
  - Achitecture: The team was able to introduce and adopt an architecture, on top of the framework that made it easy to translate for people with strong backend and OOP knowledge
  - Maintainability: Being able to come in, as a new developer on the team, and introduce meaningful work is testament of how a well architected project is easy to maintain
  - Customisability: The codeo teams successfuly extended the VueJS application through webpack to support multiple brands and designs for multiple countries while using the same codebase for the business logic
  - Modularity: Not only does the logic writen service the web application, but using the react native bridge for the mobile app, the same VueJS project leverages some native features you find either on Android or iOS to refine the end user's experience of the platform, for example better location detection using the devices GPS, and tailored push notifications.
-->

---

Defining a vue component

<!--
From the first time I touched VueJS to learn it, to using it in production, the VueJS framework has undergone a single major version update. From version 2 to version 3. And throughout, defining a component remained fairly the same.

A single file component is still rocking the iconic trio. The template, script and style blocks encapsulating and colocating the view, logic and styling of a component in the same file.

The vue team also introduced the composition api, a way to define your logic with imported API functions, along with it, the setup attribute, allowing us to compose the our logic with less boilerplate.

Alternatively, you can still use the Options API, implemented on top of the composition api, which is centered around the concept of a "component instance" (this) which aligns better with a class-based mental model. This also makes the Options API beginner friendly, but both interfaces are powered by the same underlying system.
-->

---

<!--

-->

---

<!-- reason to care -->
<!-- reason to believe -->
<!-- need to know -->
<!-- need to do -->

<!--
topics

Alternative ways of authoring components
Nuxt and Nitro: "Write once, deploy everywhere"
3rd party integrations (i.e. embedding a graphql server)
unjs packages and production use cases
Discover sli.dev

-->
