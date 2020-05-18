<template>
  <v-app>
    <Header />
    <Footer />
    <v-content>
      <router-view />
    </v-content>
  </v-app>
</template>








<script>
import Header from '@/components/Header'

export default {
  name: 'App',

  components: {
    Header,
  },
  
 
  data: () => ({
    //
  }),
};
</script>
<style>

</style>