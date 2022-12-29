<script setup>
name: 'HomePage'
</script>

<template>
  <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/about">About</RouterLink>
   </nav>

  
  <hr>

  <RouterView />
</template>

<style scoped>
 
</style>
