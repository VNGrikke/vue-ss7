<template>
  <div>
    <div>count: {{ count }}</div>
    <Child @increase="increase"/>
  </div>
</template>

<script setup>
import Child from "./child.vue";
import { ref } from 'vue'

const count = ref(0);

const increase = () => {
  count.value++;
}
</script>

<style>
</style>
