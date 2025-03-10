<script setup>
import { ref } from 'vue';

import Boton from '../components/Boton.vue';

const ultimoBoton = ref('null');

const botonPulsado = (numero) => {
  ultimoBoton.value = numero;
};

</script>

<template>
  <main>
    <h1>Calculadora</h1>
    <section>
      <div id="botones">
        <Boton v-for="n in 9" :key="n" :numero="n" @click="botonPulsado(n)" ></Boton> 
      </div>
    </section>
    <p>Has clicat al botó: {{ ultimoBoton }}</p>
  </main>
</template>

<style scoped>
#botones {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 10px;
}
</style>