<template>
  <div>
    <Child @message="handleMessage" />
  </div>
</template>

<script setup>
import { ref } from 'vue';
import Child from './child.vue';

const message = ref('');

const handleMessage = (msg) => {
  message.value = msg;
  alert(msg);
}
</script>

<style>
.alert {
  margin-top: 20px;
  padding: 15px;
  background-color: #f1f1f1;
  border: 1px solid #ccc;
  border-radius: 5px;
}
</style>
 