<template>
  <div class="scroll-wrapper" >
    <ghibli-component v-for="film in films" v-bind:key="film.id" :film="film"/>
  </div>
</template>

<script>
import ghibliService from'../service/GhibliService'
import GhibliComponent from'../components/GhibliComponent.vue'
export default {

    components: {
        GhibliComponent
    },
    data(){
        return{
            films: []
        }
    },
    created(){
        ghibliService.getMovies()
            .then((response) => {
                console.log(response)
                this.films = response.data
            })
    }
}
</script>

<style>

.scroll-wrapper {
  display: flex;
  overflow-x: auto;
  width: 100%;
  background-color: #4E1A3D;
}
</style>