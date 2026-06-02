<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const showButton = ref(false)

const handleScroll = () => {
  showButton.value = window.scrollY > 400
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})

const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: 'smooth',
  })
}
</script>

<template>
  <button
    v-if="showButton"
    @click="scrollToTop"
    class="fixed bottom-6 right-6 bg-black text-white w-12 h-12 rounded-full shadow-lg hover:opacity-90 transition z-50"
  >
    ↑
  </button>
</template>
