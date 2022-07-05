<template>
<navbar/>
  <router-view/>
  
</template>
<script>
import navbar from "./components/navbar.vue";
export default{
  components:{
    navbar,
  }
}
</script>

<style >
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: "Electrolize", sans-serif;
  scroll-behavior: smooth;
  border-width: 0;
}
#app {
  /* font-family: Avenir, Helvetica, Arial, sans-serif; */
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#logo{
  position: fixed;
  top: 0;
  left:0;
  display: flex;
  align-items: center;
}
#logo img{
width: 32px;
height: 32px;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}

</style>
