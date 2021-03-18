<template>
  <v-footer padless >
    <v-col
    
      class="text-left indigo float-left"
      cols="12"
    >

    
        <v-btn
        color="primary"
        rounded        
        > Iniciar Sessió</v-btn>

    <v-divider
    class="ma-4"
    vertical
    
    style="display: inline"
    ></v-divider>

    
     

   <v-btn
        color="primary"
        rounded
        x-small
        > Registre </v-btn>  
        
  
    </v-col>
           
    </v-footer>
</template>

<script>
import { defineComponent } from '@vue/composition-api'

export default defineComponent({
  setup() {
    
  },
})
</script>
