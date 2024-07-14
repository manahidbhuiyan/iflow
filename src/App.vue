<template>
  <div id="app">
   <header>
    <Navbar />
   </header>
   <main>
    <Home />
   </main>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Home from './components/Home.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Home,
  },
};
</script>

<style>
body {
  font-family: 'Work Sans', sans-serif;
}
/* Add any global styles if needed */
</style>

