<template>
  <div>
    <Navbar /> <router-view /> <Home /> <About /> <Destinasi />>
    <Contact />
    <Footer />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Footer from "./components/Footer.vue";
import Contact from "./components/Contact.vue";
import Destinasi from "./components/Destinasi.vue";
import About from "./components/About.vue";
import Home from "./components/Home.vue";
export default {
  name: "App",
  components: {
    Footer,
    Navbar,
    Contact,
    Destinasi,
    About,
    Home
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
