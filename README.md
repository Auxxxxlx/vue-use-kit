<p align="center">
  <br>
  <br>
  <a href="https://github.com/microcipcip/vue-use-kit">
    <img 
      src="https://raw.githubusercontent.com/microcipcip/vue-use-kit/master/public/branding/logo.png" 
      alt="Vue use kit" 
      width="200" 
    />
  </a>
  <br>
  <br>
  <br>
</p>

[![NPM Version](https://img.shields.io/npm/v/vue-use-kit.svg)](https://www.npmjs.com/package/vue-use-kit) [![NPM Downloads](https://img.shields.io/npm/dm/vue-use-kit.svg)](https://www.npmjs.com/package/vue-use-kit) [![Build Status](https://img.shields.io/travis/microcipcip/vue-use-kit/master.svg)](https://travis-ci.org/microcipcip/vue-use-kit) [![GitHub license](https://img.shields.io/github/license/microcipcip/vue-use-kit?style=flat-square)](https://github.com/microcipcip/vue-use-kit/blob/master/LICENSE)
[![Demo](https://img.shields.io/badge/demos-🚀-yellow.svg)](https://microcipcip.github.io/vue-use-kit/)

> 🛠️ Vue kit of useful [Vue Composition API](https://vue-composition-api-rfc.netlify.com) functions.</em>

Please note that Vue 3.0 has not been released yet, therefore the installation and setup of [@vue/composition-api](https://github.com/vuejs/composition-api) is required for this library to work.

## Install

```shell script
npm install @vue/composition-api vue-use-kit
```

## Setup

```
import Vue from 'vue';
import VueCompositionAPI from '@vue/composition-api';
Vue.use(VueCompositionAPI);
```

## Usage

```
<template>
  <div>isDesktop: {{ isDesktop ? 'Yes' : 'No' }}</div>
</template>

<script lang="ts">
  import Vue from 'vue'
  import { useMedia } from 'vue-use-kit'

  export default Vue.extend({
    name: 'UseMedia',
    setup() {
      const query = '(min-width: 1024px)'
      const isDesktop = useMedia(query)
      return { isDesktop }
    }
  })
</script>
```

## APIs

- Sensors
  - [`useGeolocation`](./src/components/useGeolocation/stories/useGeolocation.md) &mdash; tracks geolocation state of user's device.
    [![Demo](https://img.shields.io/badge/demo-🚀-yellow.svg)](https://microcipcip.github.io/vue-use-kit/?path=/story/sensors-usegeolocation--demo)
  - [`useHover`](./src/components/useHover/stories/useHover.md) &mdash; tracks mouse hover state of a given element.
    [![Demo](https://img.shields.io/badge/demo-🚀-yellow.svg)](https://microcipcip.github.io/vue-use-kit/?path=/story/sensors-usehover--demo)
  - [`useIntersection`](./src/components/useIntersection/stories/useIntersection.md) &mdash; tracks intersection of target element with an ancestor element.
    [![Demo](https://img.shields.io/badge/demo-🚀-yellow.svg)](https://microcipcip.github.io/vue-use-kit/?path=/story/sensors-useintersection--demo)
    [![Demo](https://img.shields.io/badge/advanced_demo-🚀-yellow.svg)](https://microcipcip.github.io/vue-use-kit/?path=/story/sensors-useintersection--advanced-demo)
  - [`useMedia`](./src/components/useMedia/stories/useMedia.md) &mdash; tracks state of a CSS media query.
    [![Demo](https://img.shields.io/badge/demo-🚀-yellow.svg)](https://microcipcip.github.io/vue-use-kit/?path=/story/sensors-usemedia--demo)
    [![Demo](https://img.shields.io/badge/advanced_demo-🚀-yellow.svg)](https://microcipcip.github.io/vue-use-kit/?path=/story/sensors-usemedia--advanced-demo)
  - [`useMouse`](./src/components/useMouse/stories/useMouse.md) &mdash; tracks the mouse position.
    [![Demo](https://img.shields.io/badge/demo-🚀-yellow.svg)](https://microcipcip.github.io/vue-use-kit/?path=/story/sensors-usemouse--demo)
    [![Demo](https://img.shields.io/badge/advanced_demo-🚀-yellow.svg)](https://microcipcip.github.io/vue-use-kit/?path=/story/sensors-usemouse--advanced-demo)
  - [`useMouseElement`](./src/components/useMouseElement/stories/useMouseElement.md) &mdash; tracks the mouse position relative to given element.
    [![Demo](https://img.shields.io/badge/demo-🚀-yellow.svg)](https://microcipcip.github.io/vue-use-kit/?path=/story/sensors-usemouseelement--demo)
- Animations
  - [`useInterval`](./src/components/useInterval/stories/useInterval.md) &mdash; updates `counter` value repeatedly on a fixed time delay.
    [![Demo](https://img.shields.io/badge/demo-🚀-yellow.svg)](https://microcipcip.github.io/vue-use-kit/?path=/story/animations-useinterval--demo)
  - [`useIntervalFn`](./src/components/useIntervalFn/stories/useIntervalFn.md) &mdash; calls function repeatedly on a fixed time delay.
    [![Demo](https://img.shields.io/badge/demo-🚀-yellow.svg)](https://microcipcip.github.io/vue-use-kit/?path=/story/animations-useintervalfn--demo)
  - [`useRaf`](./src/components/useRaf/stories/useRaf.md) &mdash; returns `elapsedTime` with requestAnimationFrame.
    [![Demo](https://img.shields.io/badge/demo-🚀-yellow.svg)](https://microcipcip.github.io/vue-use-kit/?path=/story/animations-useraf--demo)
  - [`useRafFn`](./src/components/useRafFn/stories/useRafFn.md) &mdash; calls function with requestAnimationFrame.
    [![Demo](https://img.shields.io/badge/demo-🚀-yellow.svg)](https://microcipcip.github.io/vue-use-kit/?path=/story/animations-useraffn--demo)
    [![Demo](https://img.shields.io/badge/advanced_demo-🚀-yellow.svg)](https://microcipcip.github.io/vue-use-kit/?path=/story/animations-useraffn--advanced-demo)
  - [`useTimeout`](./src/components/useTimeout/stories/useTimeout.md) &mdash; returns `isReady` true when timer is completed.
    [![Demo](https://img.shields.io/badge/demo-🚀-yellow.svg)](https://microcipcip.github.io/vue-use-kit/?path=/story/animations-usetimeout--demo)
  - [`useTimeoutFn`](./src/components/useTimeoutFn/stories/useTimeoutFn.md) &mdash; calls function when timer is completed.
    [![Demo](https://img.shields.io/badge/demo-🚀-yellow.svg)](https://microcipcip.github.io/vue-use-kit/?path=/story/animations-usetimeoutfn--demo)
- UI
  - [`useClickAway`](./src/components/useClickAway/stories/useClickAway.md) &mdash; triggers callback when user clicks outside target area.
    [![Demo](https://img.shields.io/badge/demo-🚀-yellow.svg)](https://microcipcip.github.io/vue-use-kit/?path=/story/ui-useclickaway--demo)
  - [`useFullscreen`](./src/components/useFullscreen/stories/useFullscreen.md) &mdash; display an element in full-screen mode
    [![Demo](https://img.shields.io/badge/demo-🚀-yellow.svg)](https://microcipcip.github.io/vue-use-kit/?path=/story/ui-usefullscreen--demo)
- Utils
  - [`getQuery`](./src/components/getQuery/stories/getQuery.md) &mdash; get a CSS media query string.
    [![Demo](https://img.shields.io/badge/demo-🚀-yellow.svg)](https://microcipcip.github.io/vue-use-kit/?path=/story/utils-getquery--demo)

## Inspiration

- [react-use](https://github.com/streamich/react-use)
- [vue-hooks](https://github.com/u3u/vue-hooks)
- [vue-use-web](https://github.com/logaretm/vue-use-web)

## Made with

- [Vue](https://vuejs.org/)
- [@vue/composition-api](https://github.com/vuejs/composition-api)
- [@vue/test-utils](https://vue-test-utils.vuejs.org/)
- [Jest](https://jestjs.io/)
