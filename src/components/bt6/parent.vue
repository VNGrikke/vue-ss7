<template>
  <Child>
    <template #header>
      <h3>san pham moi nhat</h3>
    </template>
    <template #body>
      <div>mo ta ngan gon ve san pham ....</div>
    </template>
    <template #footer>
      <button class="btn-detail">xem chi tiet</button>
    </template>
  </Child>
</template>

<script setup>
import Child from "./child.vue";
</script>

<style>
.btn-detail {
  margin-top: 20px;
  background-color: #007bff;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}
</style>
