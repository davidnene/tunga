<script setup>
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';
</script>

<template>
  <header>
    <div>
      <Navbar/>
    </div>
  </header>
  <RouterView />
  <Footer/>
</template>

<style>
  .cust-padding {
    padding-top: 80px;
  }
  .footer-color {
    background: #f0f5f9;
  }
</style>