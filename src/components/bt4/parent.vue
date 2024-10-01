<template>
  <div>
    <div>id: {{ id }}</div>
    <Child @delete="deleteItem"/>
  </div>
</template>

<script setup>
import Child from "./child.vue";
import { ref } from 'vue'

const id = ref("");

const deleteItem = (param) => {
  id.value = param;
}
</script>

<style>
</style>
