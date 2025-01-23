<template>
  <div class="consola">
    <h3>Consola</h3>
    <ul>
       <li v-for="(mensaje, index) in mensajesConsola" :key="index">{{ mensaje }}</li>
    </ul>
  </div>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  mensajesConsola: Array
});
</script>

<style scoped>
.consola {
  background-color: #ffffff;
  color: #333333;
  padding: 20px;
  border-radius: 10px;
  max-height: 300px;
  overflow-y: auto;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
}

.consola h3 {
  margin-top: 0;
  color: #f42e56;
  font-size: 20px;
}

.consola ul {
  list-style: none;
  padding: 0;
}

.consola li {
  margin-bottom: 10px;
  padding: 10px;
  background-color: #f7f9fc;
  border-radius: 5px;
}
</style>