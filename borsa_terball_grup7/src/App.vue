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

import Header from './components/Header';
import Buscador from './components/Buscador';
import Footer from './components/Footer';

export default {
  name: 'App',

  components: {
    Footer,
    Buscador,
    Header
  },
  
  data: () => ({
    //
  }),
};
</script>
