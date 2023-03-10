<script setup>
    const nome = 'Giulia'
    const idade = 16

    function inverter(texto) {
        return texto.split('').reverse().join('')
    }

    function saudacao() {
        return `Olá, ${nome}!`
    }

    let contador = ref(0)


function incrementarContador() {
  contador.value++
}
function decrementarContador() {
  if (contador.value > 0)
   {contador.value-- }
  
  
}
function Reiniciar() {
    contador.value = 0
  }
  onMounted(() => {
  console.log(`O valor inicial do contador é ${contador.value}.`)
})


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
    <br>
    <br>
    <button @click="incrementarContador">+</button>
  <button @click="decrementarContador">-</button>
  <button @click="Reiniciar">C</button>
  <p>Valor do contador é: {{ contador }}</p>
   
   
    <div>

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
button {
  font-weight: bold;}
  button {
  display: inline-block;
  padding: 15px 25px;
  font-size: 24px;
  margin: 20px;
  cursor: pointer;
  text-align: center;
  text-decoration: none;
  outline: none;
  color: #fff;
  background-color: #634caf;
  border: none;
  border-radius: 15px;
  box-shadow: 0 9px #999;
}
a{
color: #fff;
}

</style>