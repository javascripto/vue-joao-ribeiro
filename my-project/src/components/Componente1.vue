<template>
  <div class="container">
    <input type="text" v-model="nome" class="form-control">
    <p>O valor inserido é: {{nome}}</p>
    <button @click="limpar" class="btn btn-success">limpar</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nome: 'Yuri',
    };
  },
  methods: {
    limpar() {
      this.nome = '';
    }
  }
}
</script>
