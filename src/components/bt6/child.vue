<template>
  <div class="card">
    <slot name="header"> </slot>

    <slot name="body"></slot>

    <slot name="footer"> </slot>
  </div>
</template>

<script setup>
</script>

<style>
.card {
  border: 1px solid #ddd;
  padding: 16px;
  border-radius: 8px;
  width: 220px;
}
</style>
