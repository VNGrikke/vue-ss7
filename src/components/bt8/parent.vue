<template>
  <div>
    <button @click="showForm = true" class="add-btn">Add user</button>
    
    <Child :isVisible="showForm" @close="handleClose" />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import Child from './child.vue'

const showForm = ref(false);

const handleClose = () => {
  showForm.value = false;
};
</script>

<style >
.add-btn {
  background-color: #007bff;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

.add-btn:hover {
  background-color: #0056b3;
}
</style>
