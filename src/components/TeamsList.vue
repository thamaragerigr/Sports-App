<template>
  <div>
    <!--Header-->
    <header class="mt-12">
      <i class="fas fa-football-ball" style="color:white; font-size:170px;transform: rotate(45deg);"></i>
      <h1 class="text-white uppercase text-6xl">College Football</h1>
      <p class="text-white text-base">Encuentra los datos de tus equipos favoritos de football y compara entre ellos</p>
    </header>
    <!--Header-->

    <div class="justify-center flex wx-30 mt-8">
      <input class="rounded p-2" v-model="search" type="text" placeholder="Search..." />
      <button
        class="bg-grey-500 rounded w-auto flex justify-end items-center p-2 hover:text-blue-light"
      >
        <i class="fas fa-search text-red-500 "></i>
      </button>
    </div>

    <div id="equipos" class="flex flex-wrap justify-center mt-10">
      <div
        class="w-56 h-auto shadow-sm block bg-white rounded-lg m-4"
        v-for="team in filteredTeams"
        v-bind:key="team.school"
      >
        <div class="px-2 py-2">
          <button class="hover:text-red-600 text-red-400  px-2 my-3 float-right">
            <i class="fas fa-heart text-lg"></i>
          </button>

          <img class="h-16 w-16 rounded-full mx-auto"  :src="team.logos">
          
          <h4 class="font-bold text-grey-700 text-lg mb-2">{{ team.school }}</h4>
          <h4 class="font-bold text-grey-700 text-lg mb-2">{{ team.abbreviation }}</h4>
          <p class="text-gray-700 text-base">Mascota: {{ team.mascot }}</p>
          <p>Color: {{ team.color }}</p>
          
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import axios from "axios";

export default {
  name: "Equipos",
  data() {
    return {
      teams: [],
      search: ""
    };
  },
  created: function() {
    axios.get("https://api.collegefootballdata.com/teams").then(res => {
      this.teams = res.data;
    });
  },
  computed: {
    filteredTeams: function(){
      return this.teams.filter((team) => {
        return team.school.match(this.search)
      })
    }
  }
  
};
</script>

<style>

h1{
  font-family: 'Lato', sans-serif;
}
h4 {
  margin-bottom: 5%;
}
</style>