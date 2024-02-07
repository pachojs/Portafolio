<template>
  <div id="app">
    <div class="content">
      <nav>
        <router-link to="/">Inicio</router-link> |
        <router-link to="/about">Acerca de mi</router-link>
      </nav>
      <router-view/>
    </div>
    <thefooter />
  </div>
</template>
 
<script>
import Thefooter from './components/Thefooter.vue'; 
export default {
  components: {
    Thefooter,
    
  },
};
</script>


<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto+Mono&display=swap');

body {
  background-color:#1d1e2f !important;
  font-family: 'Roboto Mono', monospace !important;

}
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: white;
  position: relative;
  overflow: hidden;
}

.content {
  position: relative;
  z-index: 1;
}

nav {
  padding: 30px;
}

nav a {
  transition: all calc(2.5s) ease 0s;
  margin: 2%;
  padding: 2%;
  list-style: none;
  border-radius: 4px;
  margin-right: 20px;
}

nav a.router-link-exact-active {
  color: #42b983;
}

footer {
  width: 100%;
  height: 35vh;
  background: linear-gradient(to top, #000, #1d1e2f);
  color: white;
  padding: 20px;
  text-align: center;
}



</style>
