<template>
  <div>
    <input type="text" v-model="nome">
    <p>O valor inserido é: {{nome}}</p>
    <button @click="limpar">limpar</button>
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
