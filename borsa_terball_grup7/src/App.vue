<template>
  <v-app>
    <v-main>
      <Header/>
      <Buscador/>
      <Empresa/>
      <Admin/>
      <Footer/>
    </v-main>
  </v-app>
</template>

<script>

import Header from './components/Header';
import Buscador from './components/Buscador';
import Empresa from './components/Empresa';
import Admin from './components/Admin';
import Footer from './components/Footer';

export default {
  name: 'App',

  components: {
    Footer,
    Header,
    Buscador,
    Empresa,
    Admin
  },
  
  data: () => ({
    //
  }),
};
</script>
