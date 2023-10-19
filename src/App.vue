<template>
  <v-app>
    <v-main>
      <Navbar/>
      <router-view/>
      <Footer/>
    </v-main>
  </v-app>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';
export default {
  name: 'App',
  components: {Navbar, Footer,},

  data: () => ({
    //
  }),
}
</script>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@100;200;300;400;500;600;700;800;900&family=Raleway:wght@100;200;300;400;500;600;700;800;900&display=swap');
main{
  font-family: Raleway, sans-serif;

  a{
    text-decoration: none;
  }
}



</style>
