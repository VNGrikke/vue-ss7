<template>
  <div>
    <button @click="sendMessage">Send message</button>
  </div>
</template>

<script setup>
const emit = defineEmits(["message"]);

const sendMessage = () => {
  emit('message', 'Welcome to Rikkei Education');
}
</script>

<style>
button {
  padding: 10px;
  font-size: 16px;
  background-color: #f0f0f0;
  border: 1px solid #ccc;
  cursor: pointer;
}
</style>
