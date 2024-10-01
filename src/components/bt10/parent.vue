<template>
  <div>
    <Child v-model="inputValue" placeholder="Enter your name"> </Child>

    <p>Giá trị nhập vào: {{ inputValue }}</p>
  </div>
</template>

<script setup>
import { ref } from "vue";
import Child from "./child.vue";

const inputValue = ref("");

</script>

<style>

</style>