<template>
  <h2 class="main-title">我的网站导航</h2>
  <list :list="showList"></list>
</template>

<script setup>
import { reactive } from "@vue/reactivity";
import List from "./components/List.vue";
const showList = reactive([
  {
    name: "vue音乐",
    url: "./vuemusic",
    id: "vuemusic",
  },
]);
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.main-title {
  padding: 20px;
  background-color: rgb(140, 245, 240);
}
</style>
