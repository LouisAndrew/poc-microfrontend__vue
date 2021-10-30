<template>
  <div id="app">
    <h1 class="font-bold text-2xl">Hello from Vue web component!</h1>
    <div class="py-3">
      <h3 class="font-semibold text-xl">
        Current #count:
        {{ count }}
      </h3>
      <button
        type="button"
        :class="actionButtonClasses"
        @click="decrement"
      >
        Decrement
      </button>
      <button
        type="button"
        :class="actionButtonClasses"
        @click="increment"
      >
        Increment
      </button>
    </div>
    <img alt="Vue logo" src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Vue.js_Logo_2.svg/512px-Vue.js_Logo_2.svg.png">
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'App',
  data: () => ({
    count: 0,
    actionButtonClasses: 'font-bold inline-block duration-200 mt-2 px-2 py-1 rounded bg-gray-100 hover:bg-gray-200 last:ml-2',
  }),
  methods: {
    increment() {
      this.count += 1;
    },
    decrement() {
      this.count -= 1;
    },
  },
});
</script>

<style>
@tailwind base;
@tailwind components;
@tailwind utilities;
</style>
