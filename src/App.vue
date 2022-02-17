<template>
  <div id="app">
    <h1>Lista de tarefas</h1>
    <div>
      <h2>Tarefas</h2>
    </div>
    <div v-bind:key="tarefa.id" v-for="tarefa in tarefas">
      <div>
        <p v-if="tarefa.estaCompleta" id="ok">{{tarefa.id}} - {{tarefa.descricao}} -- CONCLUÍDA</p>
        <p v-else id="nOk">{{tarefa.id}} - {{tarefa.descricao}} -- PENDENTE</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "app",
  data: function(){
    return{
      title: "Locadoras de filmes",
      horas: new Date().getHours(),
      tarefas: [
          { id: 1, descricao: "Desenvolver trabalho da disciplida de Projeto de Bloco", estaCompleta: false},
          { id: 2, descricao: "Resolver o problema da aplicação do trabalho de HTML", estaCompleta: true},
          { id: 3, descricao: "Estudar de Vue para melhorar o conhecimento", estaCompleta: false},
          { id: 4, descricao: "Ir ao shopping comprar um mouse novo", estaCompleta: false},
          { id: 5, descricao: "Testar a aplicação de java", estaCompleta: true}
        ]
      };
    }
  };
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#nOk{
  color: red;
}
#ok{
  color: green;
}
</style>
