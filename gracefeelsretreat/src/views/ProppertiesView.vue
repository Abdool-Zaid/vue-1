<template>
  <div>
    <h1>Planets for sale</h1>
    <div class="container">

        <planetCard v-for="planet in planets" :key="planet.id" class="card" :planet="planet"/>
      
    
    </div>
  </div>
</template>
<script>
import planetCard from '../components/planetCard.vue'

export default {
    components:{
        planetCard
    },  
  data() {
    return {
      planets: [],
    };
  },
  mounted() {
    fetch("http://localhost:3000/planets")
      .then((res) => res.json())
      .then((data) => (this.planets = data))
      .catch((err) => console.log("error displaying planets"));
  },
};
</script>
<style>
.container{
    display: flex;
    flex-wrap: wrap;
    justify-content: space-evenly;
}

    </style>
