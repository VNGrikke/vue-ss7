<template>
  <div class="btn-list">
    <Child @click="Submit">Submit</Child>
    <Child @click="Cancel">Cancel</Child>
    <Child @click="Reset">Reset</Child>
    <div>Đã nhấn vào nút: {{ valueBtn }}</div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import Child from "./child.vue";

const valueBtn = ref("");

const Submit = () => {
  valueBtn.value = "Submit";
};

const Cancel = () => {
  valueBtn.value = "Cancel";
};

const Reset = () => {
  valueBtn.value = "Reset";
};
</script>

<style scoped>
.btn-list {
  display: flex;
  gap: 20px;
}
</style>
