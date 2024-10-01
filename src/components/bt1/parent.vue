<template>
<div>
    <div>parent company: {{company}}</div>
    <div>___________________________</div>
    <Child :company="company" />
</div>

</template>

<script setup>
import Child from "./child.vue";
const company = "Rikkei Academy";
</script>

<style>
</style>