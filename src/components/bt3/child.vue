<template>
  <button @click="$emit('increase')">increase</button>
</template>

<script setup>
const emit = defineEmits(["increase"]);
</script>

<style>
</style>
