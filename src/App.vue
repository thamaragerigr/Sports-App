<template>
  <div id="app">
    <!--Menu Component-->
    <my-menu></my-menu>
    <!--Listado de equipos-->
    <teams-list v-bind:teams="teams"></teams-list>
  </div>
</template>

<script>
import Menu from "./components/Menu";
import Teams from "./components/TeamsList";
import axios from "axios";

export default {
  name: "app",
  components: {
    "my-menu": Menu,
    "teams-list": Teams
  },
  data() {
    return {
      teams: []
    };
  },
  created: function() {
    axios.get("https://api.collegefootballdata.com/teams").then(res => {
      this.teams = res.data;
    });
  }
};
</script>

<style>
body {
  background-color: #191919;
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  font-family: "ABeeZee", sans-serif;
}
</style>
