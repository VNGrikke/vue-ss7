<template>
<div>
    <Child :product="product" />
</div>

</template>

<script setup>
import Child from "./child.vue";
const product = {
    id: 1,
    name: "Product 1",
    price: 1200,
    quantity: 12
};
</script>

<style>
</style>