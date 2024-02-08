<script setup>
import List from './components/listUsers/List.vue';
import PlusMinus from './components/plusMinus/PlusMinus.vue';
// import HelloWorld from './components/HelloWorld.vue'
// import Button from './components/Button.vue'
</script>

<template >
  <div>
    <PlusMinus />
    <List />
  </div>
  <!-- <HelloWorld msg="Vite + Vue" /> -->
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.red {
  color: red;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
