<script setup>
import Navbar from "@/components/Navbar.vue";
import Main from "@/components/Main.vue";
import Footer from "@/components/Footer.vue";
</script>

<template>
  <div class="h-screen flex flex-col">
    <Navbar class="h-[10%]" />
    <Main class="h-[85%]" />
    <Footer class="h-[5%]" />
  </div>
</template>

<style scoped></style>
