<script setup>
  defineProps({
    isActive: Boolean 
  })
</script>

<template>
  <nav class="z-40 h-14 w-full fixed top-0 flex items-center justify-between bg-gradient-to-r from-slate-800 to-slate-700 filter backdrop-blur-3xl bg-opacity-30 shadow">
    <h1 class="mx-4 text-2xl font-bold text-transparent bg-gradient-to-r from-blue-500 to-blue-300 bg-clip-text backdrop-filter backdrop-blur-md bg-opacity-30">MariaUI</h1>
    <button @click="toggleMenu" class="mx-4 text-white hover:text-blue-400 transition-all md:hidden text-2xl">
      <Icon name="ic:round-menu" v-if="!isActive" />
      <Icon name="ic:round-close" v-else />
    </button>
  </nav>
</template>

<script>
  export default {
    methods: {
      toggleMenu() {
        this.$emit('handleMenuClick', true)
      }
    }
  }
</script>