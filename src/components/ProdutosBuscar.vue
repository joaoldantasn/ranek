<template>
  <form>
    <input name="busca" id="busca" type="text" v-model="busca" />
    <input
      type="submit"
      id="lupa"
      value="buscar"
      @click.prevent="buscarProdutos"
    />
    {{ busca }}
  </form>
</template>

<script>
// @ is an alias to /src

export default {
  name: "ProdutosBuscar",
  data() {
    return {
      busca: "",
    };
  },
  methods: {
    buscarProdutos() {
      this.$router.push({ query: { q: this.busca } });
    },
  },
};
</script>
