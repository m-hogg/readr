<template>
  <div id="app" class="h-screen">
    <div class="float-left h-full" style="width: 10%">
      <navbar />
    </div>
    <div class="float-left h-full" style="width: 90%">
      <div class="w-full bg-blue-800 h-32">
        
      </div>
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
  background-color: #edf2f7;
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
