<template>
  <v-app>
    <v-main>
      <Header/>
      <Buscador/>
      <Admin/>
      <Footer/>
    </v-main>
  </v-app>
</template>

<script>

import Header from './components/Header';
import Buscador from './components/Buscador';
import Admin from './components/Admin';
import Footer from './components/Footer';

export default {
  name: 'App',

  components: {
    Footer,
    Buscador,
    Admin,
    Header
  },
  
  data: () => ({
    //
  }),
};
</script>
