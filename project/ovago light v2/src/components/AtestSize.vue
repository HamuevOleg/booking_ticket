<script setup>
  import { ref, computed, onMounted, onBeforeUnmount } from 'vue'

  const isLarge = ref(false)
  const boxRef = ref(null)

  const boxStyle = computed(() => ({
    width: isLarge.value ? '300px' : '150px',
    height: isLarge.value ? '300px' : '150px',
  }))

  const expandBox = () => {
    isLarge.value = true
  }

  const handleClickOutside = (event) => {
    if (boxRef.value && !boxRef.value.contains(event.target)) {
      isLarge.value = false
    }
  }

  onMounted(() => {
    document.addEventListener('click', handleClickOutside)
  })

  onBeforeUnmount(() => {
    document.removeEventListener('click', handleClickOutside)
  })
</script>

<template>
  
  <div
    ref="boxRef"
    :style="boxStyle"
    @click="expandBox"
    class="box"
  >
    Click Me
  </div>

</template>



<style scoped>
  .box {
    border-radius: 10px;
    background-color: black;
    cursor: pointer;
    transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
    color: azure;
    display: flex;
    align-items: center;
    justify-content: center;
  }
</style>

