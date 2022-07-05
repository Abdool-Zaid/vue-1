<template >
    <div>
          <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Electrolize&display=swap"
      rel="stylesheet"
    />
         <nav>
    <router-link to="/" id="logo">
      <img src="https://raw.githubusercontent.com/Abdool-Zaid/vue-1/main/gracefeelsretreat/src/assets/favicon-32x32.png" alt="logo">
      <H2>Gracefeel's retreat</H2></router-link> 
      <div id="navlinks">

          <router-link to="/">Home</router-link> 
    <router-link to="/about">About</router-link>
    <router-link to="/admin">admin</router-link>
    <router-link to="/propperties">listings</router-link>
      </div>
  </nav>
    </div>
    
</template>
<script>
export default {
    
}
</script>
    
    <style>
    * {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: "Electrolize", sans-serif;
  scroll-behavior: smooth;
  border-width: 0;
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
#navlinks{
    display: flex;
    justify-content: flex-end;
}
#navlinks > *{
    margin: 1%;

}

@media only screen and (max-width: 560px){
#navlinks{
    display: none;
    flex-direction: column;
}
#logo{
    size: 45px;
}
}
</style>