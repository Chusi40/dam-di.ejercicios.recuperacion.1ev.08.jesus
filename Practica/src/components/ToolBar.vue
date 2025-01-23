<template>
  <div class="button-container">
      <button @click="$emit('crearNota')"><font-awesome-icon icon="square-plus" /> Nueva</button>
      <button @click="$emit('clonarNotas')"><font-awesome-icon icon="clone" /> Copiar</button>
      <button @click="$emit('borrarNotas')"><font-awesome-icon icon="square-minus" /> Borrar</button>
      <button @click="$emit('limpiarNotas')"><font-awesome-icon icon="trash" /> Limpiar</button>
      <button @click="$emit('seleccionarTodo')"><font-awesome-icon icon="square-check" /> Seleccionar</button>
      <button @click="$emit('invertirSeleccion')"><font-awesome-icon icon="arrow-up-short-wide" /> Invertir</button>
      <button @click="$emit('anularSeleccion')"><font-awesome-icon icon="window-restore" /> Anular</button>
      <button @click="$emit('debug')"><font-awesome-icon icon="bug" /> Debug</button>
      <button @click="$emit('limpiarConsola')"><font-awesome-icon icon="broom" /> Limpiar</button>
      <button @click="$emit('abrirConsola')"><font-awesome-icon icon="desktop" /> Consola</button>
      <button @click="$emit('reload')"><font-awesome-icon icon="rotate-right" /> Recargar</button>
  </div>
</template>

<script setup>
import { defineEmits } from 'vue';

const emit = defineEmits([
'crearNota',
'clonarNotas',
'borrarNotas',
'limpiarNotas',
'seleccionarTodo',
'invertirSeleccion',
'anularSeleccion',
'debug',
'limpiarConsola',
'abrirConsola',
'reload'
]);
</script>

<style scoped>
.button-container {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  justify-content: center;
  background-color: #ffffff;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
}
button {
  background-color: #4a721d;
  color: #ffffff;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  font-size: 14px;
  text-transform: uppercase;
  cursor: pointer;
  transition: background-color 0.3s, box-shadow 0.3s;
}

button:hover {
  background-color: #490e1b;
  box-shadow: 0px 4px 12px rgba(244, 46, 86, 0.3);
}

button font-awesome-icon {
  margin-right: 8px;
  font-size: 18px;
}
</style>