<template>
  <div class="about">
    <div class="wrapper">
      <h5>Dados Pessoais</h5>
      <hr />
      <span> Nome: Jean Carlos de Andrade Vieira </span>
      <span> Idade: 20 </span>
      <span> Email: jeancarlos.av0@gmail.com </span>
      <br />
      <div class="escolaridade">
        <h5>Escolaridade</h5>
        <hr />
        <span> Tecnólogo: Análise e Desenvolvimento de Sistemas </span>
        <span> Status: Cursando </span>
        <span> Termo: 3º </span>
        <span> Turma: A </span>
        <span> Instituição de Ensino: Unimar </span>
      </div>
    </div>
  </div>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=JetBrains+Mono:ital,wght@0,100..800;1,100..800&display=swap");

* {
  margin: 0;
  padding: 0;
}

.about {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: aliceblue;
  font-family: "JetBrains Mono", sans-serif;
}

.wrapper {
  display: block;
  justify-content: center;
  border: 1px solid black;
  padding: 15px;
}

h5 {
  font-style: italic;
  font-size: 18px;
}

span {
  font-size: 15px;
  display: block;
}
</style>