<script setup>
defineProps({
  msg: {
    type: String,
    required: true,
  },
});
const appName = import.meta.env.VITE_APP_NAME;
const appDescription = import.meta.env.VITE_APP_DESCRIPTION;
const gaID = import.meta.env.VITE_GA_ID;
</script>

<template>
  <div class="greetings">
    <h1 class="green">{{ msg }}</h1>
    <h3>App Name: {{ appName }}</h3>
    <h3>App Description: {{ appDescription }}</h3>
    <h3>GA ID: {{ gaID }}</h3>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
