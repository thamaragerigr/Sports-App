<template>
  <div id="app">
    <!--Menu Component-->
    <my-menu></my-menu>
    <!--Listado de equipos-->
   <teams-list></teams-list>


  </div>
</template>

<script>
import Menu from "./components/Menu";
import Teams from "./components/TeamsList"

export default {
  name: "app",
  components: {
    "my-menu": Menu,
    "teams-list": Teams
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
