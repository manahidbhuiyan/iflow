<template>
  <div id="app">
    <header>
      <Navbar />
    </header>
    <main>
      <Home />
    </main>
    <Footer />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Home from "./components/Home.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Navbar,
    Home,
    Footer,
  },
};
</script>

<style>
body {
  font-family: "Work Sans", sans-serif;
}
/* Add any global styles if needed */
</style>

