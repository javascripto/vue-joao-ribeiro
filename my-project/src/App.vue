<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <Novo></Novo> -->
    <!-- <Componente1 /> -->

    <div>Sou o componente App</div>
    <ComponenteVerde/>
    <ComponenteVermelho/>
  </div>
</template>

<script>
import Novo from './components/Novo'
import HelloWorld from './components/HelloWorld'
import Componente1 from './components/Componente1'
import ComponenteVerde from './components/ComponenteVerde';
import ComponenteVermelho from './components/ComponenteVermelho';

// Vue.components('component-1', Componente1);


export default {
  name: 'app',
  components: {
    Novo,
    HelloWorld,
    Componente1,
    ComponenteVerde,
    ComponenteVermelho,
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
