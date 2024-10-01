<template>
  <div class="item-list">
    <Child @click="handleClick(1)" :class="{ active: activeItem === 1 }">Item 1</Child>
    <Child @click="handleClick(2)" :class="{ active: activeItem === 2 }">Item 2</Child>
    <Child @click="handleClick(3)" :class="{ active: activeItem === 3 }">Item 3</Child>

    <div>Đã nhấn vào item: {{ valueItem }}</div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import Child from "./child.vue";

const valueItem = ref(1); 
const activeItem = ref(1); 

const handleClick = (index) => {
  valueItem.value = index;  
  activeItem.value = index;
};
</script>

<style scoped>
.item-list {
  display: flex;
  gap: 20px;
}
</style>
