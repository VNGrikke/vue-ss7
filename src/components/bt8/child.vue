<template>
  <div v-if="isVisible" class="modal-overlay">
    <div class="modal">
      <h2>Form Add User</h2>
      <div class="form-group">
        <label>Name</label>
        <input type="text" v-model="name" />
      </div>
      <div class="form-group">
        <label>Email</label>
        <input type="email" v-model="email" />
      </div>
      <div class="form-group">
        <label>Address</label>
        <input type="text" v-model="address" />
      </div>
      <button @click="closeForm" class="close-btn">Close</button>
    </div>
  </div>
</template>

<script setup>
import { ref, watch } from "vue";

const props = defineProps({
  isVisible: Boolean,
});

const emit = defineEmits(["close"]);

const name = ref("");
const email = ref("");
const address = ref("");

const closeForm = () => {
  emit("close");
};
</script>

<style scoped>

.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.6); 
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}


.modal {
  background-color: white;
  padding: 30px;
  border-radius: 12px; 
  width: 400px;
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1); 
  transition: transform 0.3s ease, opacity 0.3s ease; 
  transform: scale(1);
  opacity: 1;
}

h2 {
  font-size: 24px;
  color: #333;
  margin-bottom: 20px;
  text-align: center;
}

.form-group {
  margin-bottom: 20px;
}

label {
  font-size: 14px;
  color: #555;
  margin-bottom: 5px;
  display: block;
}

input {
  width: 100%;
  padding: 10px;
  font-size: 14px;
  border: 1px solid #ddd;
  border-radius: 8px;
  outline: none;
  transition: border-color 0.3s;
}

input:focus {
  border-color: #007bff;
}

.close-btn {
  background-color: #f44336; 
  color: white;
  padding: 10px 20px;
  font-size: 16px;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  width: 100%;
  margin-top: 20px;
  transition: background-color 0.3s;
}

.close-btn:hover {
  background-color: #d32f2f; 
}

.modal-enter-active, .modal-leave-active {
  opacity: 1;
  transform: scale(1);
}

.modal-enter, .modal-leave-to {
  opacity: 0;
  transform: scale(0.9);
}
</style>
