<script setup>
import Navbar from './components/Navbar.vue';
</script>

<template>
  <header>
    <div>
      <Navbar/>
    </div>
  </header>
  <RouterView />
  <footer class="sticky-bottom">
    <p>This is the footer</p>
  </footer>
</template>

<style>
  .cust-padding {
    padding-top: 80px;
  }
</style>