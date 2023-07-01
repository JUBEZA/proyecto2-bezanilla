<template>
  <div id="app">
    <router-view />
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {

  },
  created() {
    this.$store.dispatch('cargarInventario');
  },
}

</script>


<style>
body {
  background-image: url(https://images.unsplash.com/photo-1456425731181-2152d80d946c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1471&q=80); background-position: center;;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #0c7ef0;
  margin-top: 60px;
}

@import'~bootstrap/dist/css/bootstrap.css'
</style>
