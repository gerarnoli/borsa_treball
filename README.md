# Enunciat - Projecte 3
https://campus.institutpedralbes.cat/mod/url/view.php?id=118092

# API
https://github.com/mevdschee/php-crud-api

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
