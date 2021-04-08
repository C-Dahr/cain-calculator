<template>
    <v-app-bar app color="#3b3635" dark>
        <div class="d-flex align-center">
            <v-img
                alt="Cain"
                class="mr-2"
                contain
                src="https://www.spriters-resource.com/resources/sheet_icons/61/64589.png"
                transition="scale-transition"
                width="100"
            />
            <span class="title text--h4">
              Cain's Calculator
            </span>
        </div>
        <v-spacer></v-spacer>
    </v-app-bar>
</template>

<script>

export default {
  name: 'Navbar',
  components: {
  },
  data: () => ({
  })
}

</script>

<style>

#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
}

#nav {
    padding: 30px;
}

#nav a {
    font-weight: bold;
    color: #2c3e50;
}

#nav a.router-link-exact-active {
    color: #42b983;
}

</style>
