<template >
    <div class="planetCard">
    <img :src="planet.image"    class=planetImage/>

        <img :src="planet.populationURL" class="planetPopulation"/>
      <h2>{{ planet.atmosphere }}</h2>
      <h2>{{ planet.moons }}</h2>
      <h2>{{ planet.tempRange }}</h2>
      <h2>{{ planet.water }}</h2>
      <h2>{{ planet.size }}</h2>
      <h2>{{ planet.population }}</h2>
      
      <h2>{{ planet.name }}</h2>
      <h2>{{ planet.price }}</h2>
    </div>
        

</template>
<script>
export default {
    props:['planet']
}
</script>
<style >
    .planetCard{
    background-color: #efefef;
    width: fit-content;
    margin: 1em;
    padding: 1%;
    border-radius: 50px;
background: #efefef;
box-shadow:  20px 20px 60px #cbcbcb,
             -20px -20px 60px #ffffff;
}
</style>