<template>
  <div>
    <p class="item" @click="handleClick">
      <slot></slot>
    </p>
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
.item {
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

.active {
  border-bottom: 2px solid #007bff;
}
</style>
