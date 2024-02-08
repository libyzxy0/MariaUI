<script setup>
  const isMenuOpen = ref(false);
  const toggleMenu = () => {
    isMenuOpen.value = !isMenuOpen.value;
  }
</script>
<template>
  <div>
    <Sidebar :isActive="isMenuOpen" /> 
    <Navbar @handleMenuClick="toggleMenu" :isActive="isMenuOpen" />
    <slot />
  </div>
</template>