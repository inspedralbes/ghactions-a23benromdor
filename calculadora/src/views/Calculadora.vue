<script setup>
import { ref } from 'vue';

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
        <button v-for="n in 9" :key="n" :numero="n" @click="botonPulsado(n)">{{ n }}</button>
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