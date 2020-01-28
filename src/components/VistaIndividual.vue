<template>
  <div id="vistaIndividual" class="flex justify-center m-8">
    <div class="max-w-sm w-1/2 lg:max-w-full lg:flex justify-center">
      <div
        class="border-r border-b border-l border-gray-400 lg:border-l-0 lg:border-t lg:border-gray-400 bg-white rounded-b rounded-lg p-4 flex flex-col justify-between leading-normal"
      >
        <div class="mb-8 justify-center">
        <img class=" justify-center " src="https://images.pexels.com/photos/3591569/pexels-photo-3591569.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500" alt="">
          <div class="text-gray-900 font-bold text-xl mb-2 mt-4">team.school</div>
          <p class="text-gray-700 text-base">
          Mascot: { team.mascot } <br>
          Abbreviation: { team.mascot } <br>
          Alternative Names: { team.alt_name } <br> 
          Conference: { team.conference } <br>
          Division: { team.division } <br>
          </p>
        </div>
        <div class="flex items-center justify-center -mt-8">
         <div class="text-sm ">
            <p class="text-gray-900 leading-none mr-2">Colors</p>
          </div>
          <img
            class="w-8 h-8 rounded-full mr-4"
            src="https://images.pexels.com/photos/3591569/pexels-photo-3591569.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500"
            alt="Avatar of Jonathan Reinink"
          />
        </div>
      </div>
    </div>
  </div>
</template>


<script>
export default {

};
</script>


<style>
</style>