<template>
  <Child>
    <template #header>
      <h3>Thông báo từ hệ thống</h3>
    </template>
    <div>Đây là nội dung của modal. Bạn có thể đóng modal bằng cách nhấn vào nút Close.</div>
  </Child>
</template>

<script setup>
import Child from './child.vue';
</script>

<style>

</style>
