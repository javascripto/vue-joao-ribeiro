<template>
  <div class="row box1 mt-3 p-3">O meu nome é: {{name}} | {{name2}}</div>
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
  }
};
</script>

<style scoped>
.box1 {
  border: 1px solid black;
  background-color: rgb(180, 180, 180);
}
</style>
