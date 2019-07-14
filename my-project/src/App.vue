<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <Novo></Novo> -->
    <!-- <Componente1 /> -->

    <!-- <div>Sou o componente App</div> -->
    <!-- <ComponenteVerde/> -->
    <!-- <ComponenteVermelho/> -->

    <div class="container mt-3 box">
      <div class="row">
        <div class="col-12 p-4">
          <p>Mecanismo para alterar o valor do nome.</p>
          <button class="btn btn-success" @click="changeName">Alterar nome</button>
          <Detalhe :name="name" ref="detalhes" @changeName="changeName2($event)"/>
        </div>
      </div>
    </div>


  </div>
</template>

<script>
// import Novo from './components/Novo'
// import HelloWorld from './components/HelloWorld'
// import Componente1 from './components/Componente1'
// import ComponenteVerde from './components/ComponenteVerde';
// import ComponenteVermelho from './components/ComponenteVermelho';

import Detalhe from './components/Detalhe';

// Vue.components('component-1', Componente1);


export default {
  name: 'app',
  components: {
    // Novo,
    // HelloWorld,
    // Componente1,
    // ComponenteVerde,
    // ComponenteVermelho,
    Detalhe
  },
  data() {
    return {
      name: 'João'
    }
  },
  methods: {
    changeName() {
      this.name = 'Carlos'; // Alterando valor no componente filho por props
      this.$refs.detalhes.name2 = 'Carlos'; // Alterando vaor no componente filho diretamente por referencia
    },
    changeName2(event) {
      this.name = this.$refs.detalhes.name2 = event;
    }
  }
}
</script>

<style scoped>
  .box {
    border: 2px solid black;
    background-color: rgb(200, 200, 200);
  }
</style>
