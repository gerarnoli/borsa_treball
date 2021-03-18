<template>
  <v-app>
    <v-main>
      <Header/>
       <Buscador/>
      <Footer/>
     

    </v-main>
  </v-app>
</template>

<script>

import Footer from './components/Footer';
import Header from './components/Header';
import Buscador from './components/Buscador';

export default {
  name: 'App',

  components: {
    Footer,
    Header,
    Buscador
  },

  data: () => ({
    //
  }),
};
</script>
