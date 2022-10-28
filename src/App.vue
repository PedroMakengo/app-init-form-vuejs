<template>
  <div class="app">
    <h1>Fazer cadastro</h1>

    <div>
      <form action="">
        <label for="">Nome</label>
        <input type="text" v-model="user.nome" /> <br />

        <label for="">Email</label>
        <input type="email" v-model="user.email" /><br />

        <label for="">Qtd Funcionários</label>
        <input type="number" v-model="user.qtFunc" /><br />

        <label for="">Opinião</label>
        <textarea v-model="opiniao"></textarea> <br />

        <label for="">Tecnologias</label>
        <span>
          <input type="checkbox" value="javascript" v-model="tecnologias" />
          JavaScript
        </span>
        <span>
          <input type="checkbox" value="Css" v-model="tecnologias" />
          Css
        </span>
        <span>
          <input type="checkbox" value="VueJs" v-model="tecnologias" />
          VueJs </span
        ><br />

        <label for="">Qual tipo de contratação</label>
        <select v-model="tipoSelecionado">
          <option v-for="item in tipos" :key="item.id" :value="item.nome">
            {{ item.nome }}
          </option>
        </select>
        <br />
      </form>
    </div>

    <hr />
    <div class="item">
      <h2>Usuário cadastrado</h2>

      <label for="">Nome: {{ user.nome }}</label> <br />
      <label for="">Email: {{ user.email }}</label> <br />
      <label for="">Qtd Funcionários : {{ user.qtFunc }}</label> <br />
      <label for="">Sua opinião: {{ opiniao }}</label> <br />
      <label for="">Tecnologias:</label> <br />
      <ul>
        <li v-for="tech in tecnologias" :key="tech">{{ tech }}</li>
      </ul>
      <label>Tipo de Contratação: {{ tipoSelecionado }}</label> <br />
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      user: {
        nome: "",
        email: "",
        qtdFunc: 0,
      },
      opiniao: "",
      tecnologias: [],
      tipos: [
        { id: 1, nome: "Freelancer" },
        { id: 2, nome: "CLT" },
        { id: 3, nome: "PJ" },
        { id: 4, nome: "Remoto" },
      ],
      tipoSelecionado: "Freelancer",
    };
  },
};
</script>

<style>
form {
  display: flex;
  flex-direction: column;
}
</style>
