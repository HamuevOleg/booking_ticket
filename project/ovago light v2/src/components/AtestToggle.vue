<script setup>
  import { ref } from 'vue'

  const isModalOpen = ref(false)

  const openModal = () => {
    isModalOpen.value = true
  }

  const closeModal = () => {
    isModalOpen.value = false
  }
</script>

<template>
  <div>
    <button @click="openModal">Open Modal</button>

    <div v-if="isModalOpen" class="modal-overlay" @click.self="closeModal">
      <div class="modal-content">
        <h2>This is a modal!</h2>
        <p>Click outside this box to close.</p>
        <button @click="closeModal">Close</button>
      </div>
    </div>
  </div>
</template>



<style scoped>
  .modal-overlay {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: rgba(0, 0, 0, 0.5);
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 999;
  }

  .modal-content {
    background: white;
    padding: 2rem;
    border-radius: 8px;
    max-width: 400px;
    width: 100%;
  }
</style>
