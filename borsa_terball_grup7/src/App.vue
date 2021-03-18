<template>
  <v-app>
    <v-main>
      <Header/>
       <Buscador/>
       <Empresa/>
      <Footer/>
    </v-main>
  </v-app>
</template>

<script>

import Footer from './components/Footer';
import Header from './components/Header';
import Buscador from './components/Buscador';
import Empresa from './components/Empresa';

export default {
  name: 'App',

  components: {
    Footer,
    Header,
    Buscador,
    Empresa
  },

  data: () => ({
    //
  }),
};
</script>
