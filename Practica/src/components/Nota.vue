<template>
  <div class="nota-container">
    <div v-for="(nota, index) in notas" :key="nota.id" 
    :class="['nota-card', { 'nota-seleccionada': notasMarcadas.includes(index) }]">
      <p><strong>{{ nota.id }}</strong></p>
      <h3>{{ nota.titulo }}</h3>
      <p>{{ nota.descripcion }}</p>
      <div class="nota-actions">
        <button @click="$emit('borrarNota', index)">Borrar</button>
        <button @click="$emit('clonarNota', index)">Clonar</button>
        <button @click="$emit('marcarNota', index)">Marcar</button>
      </div>
    </div>
  </div>
</template>

<script setup>
import { defineProps, defineEmits } from 'vue';

const props = defineProps({
notas: Array,
notasMarcadas: Array
});

const emit = defineEmits(['borrarNota', 'clonarNota', 'marcarNota']);
</script>

<style scoped>
.nota-container {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  padding: 20px;
  background-color: #f7f9fc;
  border-radius: 10px;
}

.nota-card {
  width: 180px;
  padding: 20px;
  background-color: #ffffff;
  border: 1px solid #e0e0e0;
  border-radius: 10px;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.05);
  display: flex;
  flex-direction: column;
  align-items: center;
  color: #333333;
  transition: transform 0.2s;
}

.nota-card:hover {
  transform: translateY(-5px);
  box-shadow: 0px 8px 15px rgba(0, 0, 0, 0.1);
}

.nota-seleccionada {
  border-color: #f42e56;
  box-shadow: 0px 4px 12px rgba(244, 46, 86, 0.2);
}

.nota-card h3 {
  font-size: 18px;
  margin-bottom: 8px;
  color: #23668a;
}

.nota-actions {
  display: flex;
  gap: 10px;
  margin-top: 10px;
}

.nota-actions button {
  background-color: #227765;
  color: #ffffff;
  border: none;
  padding: 8px 12px;
  border-radius: 5px;
  font-size: 14px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.nota-actions button:hover {
  background-color: #531447;
}
</style>