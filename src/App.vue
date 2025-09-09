<script setup lang="ts">
import Navbar from "./components/Navbar.vue";
import Footer from "./components/Footer.vue";
import Exercice1 from "./components/Exercice1.vue";
import Graph from "./components/Graph.vue";
</script>

<template>
  <div class="h-screen w-screen flex flex-col">
    <Navbar />
    <main class="flex flex-col flex-1 items-center justify-center bg-gray-800">
      <router-view />
    </main>
    <Footer />
  </div>
</template>
