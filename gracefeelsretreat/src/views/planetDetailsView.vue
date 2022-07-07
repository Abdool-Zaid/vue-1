<template>
  <div >
    <div v-if="planet">
      <h1>Detailed breakdown of planet features</h1>
      <p>id = {{ $route.params.id }}</p>
         <img :src="planet.populationURL" class="planetPopulation"/>
      <h1>{{ planet.name }}</h1>
      <h2>{{ planet.atmosphere }}</h2>
      <h2> amount of moons: {{ planet.moons }}</h2>
      <h2>{{ planet.tempRange }}</h2>
      <h2>{{ planet.water }}</h2>
      <h2>size: {{ planet.size }}</h2>
      <h2>{{ planet.population }}</h2>
      
      <h2>{{ planet.price }}</h2>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      planet: null,
    };
  },
  mounted() {
    fetch("http://localhost:3000/planets/" + this.$route.params.id)
      .then((res) => res.json())
      .then((data) => {
        this.planet = data;
      });
  },
};
</script>
<style lang=""></style>
