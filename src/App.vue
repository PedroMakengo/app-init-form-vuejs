<template>
  <div class="app">
    <h1>Fazer cadastro</h1>

    <div>
      <form action="">
        <label for="">Nome</label>
        <input type="text" v-model="nome" /> <br />
      </form>
    </div>

    <hr />
    <div class="item">
      <h2>Usuário cadastrado</h2>

      <label for="">Nome: {{ nome }}</label>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      nome: "",
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
