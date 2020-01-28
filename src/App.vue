<template>
  <div id="app">
    <!--Menu Component-->
    <my-menu></my-menu>
    <!--Listado de equipos-->
   <favorites-list></favorites-list>


  </div>
</template>

<script>
import Menu from "./components/Menu";
import Favotires from "./components/Favorites"

export default {
  name: "app",
  components: {
    "my-menu": Menu,
    "favorites-list": Favotires
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
