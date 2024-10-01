<template>
  <div>
    du lieu trong child
    <div>id: {{props.product.id}}</div>
    <div>name: {{props.product.name}}</div>
    <div>price: {{props.product.price}} d</div>
    <div>quantity: {{props.product.quantity}}</div>
  </div>
</template>

<script setup>
const props = defineProps(["product"]);
</script>

<style>
</style>