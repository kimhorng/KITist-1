<template>
  <v-app>
    <v-card>
      <NavBar/>
    </v-card>
    <v-card height="90%" width="full" color="grey"></v-card>
    <v-footer dark>
      <Footer/>
    </v-footer>
  </v-app>
</template>

<script>
import Footer from './Layouts/Footer';
import NavBar from './Layouts/NavBar';
export default {
  name: 'App',

  components: {
    NavBar,
    Footer,
  },

  data: () => ({
    //
  }),
};
</script>
