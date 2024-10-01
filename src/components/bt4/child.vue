<template>
  <div class="delete-list">
    <button v-for="id in ids" :key="id" @click="$emit('delete', id)">
      delete {{ id }}
    </button>
  </div>
</template>

<script setup>
const emit = defineEmits(["delete"]);
const ids = [2, 3, 5, 8, 9, 11];
</script>

<style>
.delete-list {
  display: flex;
  gap: 10px;

}
</style>
