# borsa_treball

* Paleta de Colores: https://coolors.co/829fa8-1a5061-111414-bcdae3-5b94a6

* BBDD -> treball
* User ->  a16pednieper_g7
* PSWD -> ausias


# bootstrap vue

* plugin bootstrap-vue.js

import Vue from 'vue'
import { BootstrapVue, IconsPlugin } from 'bootstrap-vue'

// Import Bootstrap an BootstrapVue CSS files (order is important)
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

// Make BootstrapVue available throughout your project
Vue.use(BootstrapVue)
// Optionally install the BootstrapVue icon components plugin
Vue.use(IconsPlugin)

* main.js

import Vue from 'vue'
import App from './App.vue'
import vuetify from './plugins/vuetify';
import "./plugins/bootstrap-vue";

Vue.config.productionTip = false

new Vue({
  vuetify,
  render: h => h(App)
}).$mount('#app')
