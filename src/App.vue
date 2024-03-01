<script setup>

import { ref } from 'vue'
const contador = ref(0)

function decrementar() {
  if(contador.value < 1){
  alert(`O valor do contador não pode ser ZERO.`)
}
else{
  contador.value--
}
}
const nome = 'Enrique'
    const idade = 16

    function inverter(texto) {
        return texto.split('').reverse().join('')
    }

    function saudacao() {
        return `Olá, ${nome}!`
    }

function resetar(){
  contador.value = 0;
}

</script>

<template>
    
<div class="info">
        <h1>Exemplo 1 - Mostrando informações na tela</h1>
        <p>Nome: {{ nome }} </p>
        <p>Idade: {{ idade }}  anos</p>
        <hr />
        <p>Para completar 50 anos faltam: {{ 50 - idade }}  anos</p>
        <p>O nome tem {{ nome.length }}  caracteres</p>
        <p>O nome invertido é: {{ inverter(nome.toUpperCase()) }} </p>
        <hr />
        <p> Exemplo de saudação usando função</p>
        <p> {{ saudacao() }}  </p>
  </div>

<div class="cont">
 <button @click="contador++">+</button>
 <button @click="decrementar">-</button>
 <button @click="resetar">Resetar</button>
 <p> Valor do contador: {{ contador }}</p>
</div>
</template>


<style scoped>

button{
  font-weight: bold;
  margin-left: 5%;
  background-color: rgb(43, 226, 134);
  color: rgb(27, 27, 27);
  width: 25%;
  height: 25%;
  align-items: center;
}

.cont p{
  text-align: center;
}


.cont{
  background-color: rgb(0, 0, 0);
  color: white;
  padding: 50px;
  border-radius:10px ;
  margin-left: 2%;
}

.info {
  background-color: rgb(0, 0, 0);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
}

h1 {
  color: white;
  font-weight: bold;
  font-size: 1.5em;
}

</style>
