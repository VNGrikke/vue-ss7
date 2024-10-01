<template>
  <div>
    <button class="btn" @click="handleClick">
      <slot></slot>
    </button>
  </div>
</template>

<script setup>
import { ref } from "vue";

const props = defineProps(["message"]);
const emit = defineEmits(["click"]);

const handleClick = () => {
  emit("click");
};
</script>

<style scoped>
.btn {
  background-color: #007bff;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

.btn:hover {
  background-color: #0056b3;
}
</style>
