<template>
  <v-app>
    <Navbar/>
      <v-main>
        <router-view/>
      </v-main>
  </v-app>
</template>

<script>
import Navbar from '@/components/Navbar.vue'

export default {
  name: 'App',
  components: {
    Navbar
  },
  data: () => ({
  })
}

</script>

<style>

.v-main__wrap {
  background: url('assets/floor.png') no-repeat fixed !important;
  background-size: cover !important;
  background-position: center top !important;
}

</style>
