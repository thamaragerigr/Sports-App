<template>
  <div id="app">
    <!--Menu Component-->
    <my-menu></my-menu>
    <!--Listado de equipos-->
   <listado-favoritos></listado-favoritos>


  </div>
</template>

<script>
import Menu from "./components/Menu";
import Favoritos from "./components/ListadoDeFavoritos"

export default {
  name: "app",
  components: {
    "my-menu": Menu,
    "listado-favoritos": Favoritos
  }
};
</script>

<style>
body{
    background-color: #191919;
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  font-family: 'ABeeZee', sans-serif;
}

</style>
