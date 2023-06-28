<template>
  <NavBar />
  <router-view/>
  <Footer />
</template>

<script>
import NavBar from './components/NavBar.vue';
import Footer from './components/Footer.vue';

export default{
  components: { NavBar, Footer }
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
  overflow-x: hidden;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  background: #333;
}

nav {
  padding: 30px;
}
</style>
