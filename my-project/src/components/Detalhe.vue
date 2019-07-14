<template>
  <div class="row box1 mt-3 p-3">
    O meu nome é: {{name}} | {{name2}}
    <button class="btn btn-success" @click="changeName">Alterar de novo</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name2: "João"
    };
  },
  // props: ["name"],
  props: { // Detalhes de cada prop
    name: {
      type: String,
      // type: [String, Number],
      required: true,
      default: 'Fulano'
    }
  },
  methods: {
    changeName() {
      this.$emit('changeName', 'João');
    }
  }
};
</script>

<style scoped>
.box1 {
  border: 1px solid black;
  background-color: rgb(180, 180, 180);
}
</style>
