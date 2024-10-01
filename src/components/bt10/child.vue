<template>
  <div class="input-wrapper">
    <input
      :type="type"
      :placeholder="placeholder"
      :value="modelValue"
      @input="$emit('update:modelValue', $event.target.value)"
      class="custom-input"
    />
  </div>
</template>

<script setup>
const props = defineProps({
  placeholder: {
    type: String,
    default: "Enter value",
  },
  type: {
    type: String,
    default: "text",
  },
  modelValue: {
    type: [String, Number],
    default: "",
  },
});

const emit = defineEmits(["update:modelValue"]);
</script>

<style scoped>
.input-wrapper {
  display: flex;
  align-items: center;
  border: 1px solid #ccc;
  padding: 5px;
  border-radius: 5px;
}

.custom-input {
  flex: 1;
  padding: 8px;
  border: none;
  outline: none;
}
</style>
