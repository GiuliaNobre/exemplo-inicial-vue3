<script setup>
    const nome = 'Giulia'
    const idade = 16

    function inverter(texto) {
        return texto.split('').reverse().join('')
    }

    function saudacao() {
        return `Olá, ${nome}!`
    }
</script>

<template>
    <div class="info">
        <h1>Exemplo 1 - Mostrando informações na tela</h1>
        <p>Nome: {{ nome }} </p>
        <p>Idade: {{ idade }} anos</p>
        <hr />
        <p>Para completar 50 anos faltam: {{ (50-idade) }} anos</p>
        <p>O nome tem {{ nome.length }} caracteres</p>
        <p>O nome invertido é: {{ inverter(nome).toUpperCase() }} </p>
        <hr />
        <p> {{ saudacao() }}</p>
        
        
      
    </div>
</template>

<style scoped>
.info {
  background-color: rgb(96, 43, 182);
  padding: 20px 30px;
  color: rgb(255, 255, 255);
  border-radius: 10px;
}

h1 {
  color: rgb(228, 226, 228);
  font-weight: bold;
  font-size: 1.5em;
}
</style>