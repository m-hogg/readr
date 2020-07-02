<template>
  <div id="app" class="h-screen bg-gray-200">
    <div class="float-left h-full" style="width: 10%">
      <navbar />
    </div>
    <div class="float-left" style="width: 90%">
      <router-view />
    </div>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue';

export default {
  components: {
    Navbar
  },
}
</script>

<style>
body {
  height: 100%;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
