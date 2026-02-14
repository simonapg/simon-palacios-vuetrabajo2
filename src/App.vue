<template>
  <div id="app">
    <h1>Ficha de mascota</h1>
    <PetCard :mascota="mascota" />
  </div>
</template>

<script>
import PetCard from './components/PetCard.vue'

export default {
  name: 'App',
  components: {
    PetCard
  },
  data() {
    return {
      mascota: {
        nombre: 'Tanza',
        tipo: 'Perro',
        edad: 12,
        vacunado: true,
        foto: require('./assets/tanza.jpeg'),
        caracteristicas: ['Regalona', 'Obediente', 'Le dan los 5 minutos (correr mucho)']
      }
    }
  }
}
</script>

<style>
#app {
  font-family: Arial, sans-serif;
  color: #2c3e50;
  margin: 24px;
}

img {
  max-width: 300px;
  width: 100%;
  height: auto;
  border-radius: 8px;
}

ul {
  padding-left: 20px;
}
</style>
