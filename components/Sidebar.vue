<template>
  <aside class="fixed z-20 transition-all duration-300 md:border-r-2 md:border-gray-700 h-screen bg-slate-700 border-r-2 w-[15rem] md:w-[30%] md:left-0" :class="props.isActive ? ' border-gray-600 left-0' : 'border-transparent left-[-21rem]'">
    
    <div class="mt-16 relative">
     
    </div>
    
  </aside>
</template>
<script setup>
  const props = defineProps({
    isActive: Boolean
  })
</script>