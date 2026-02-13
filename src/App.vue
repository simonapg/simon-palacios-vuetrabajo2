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
        nombre: 'Luna',
        tipo: 'Perro',
        edad: 4,
        vacunado: true,
        foto: 'https://images.unsplash.com/photo-1517849845537-4d257902454a?auto=format&fit=crop&w=600&q=80',
        caracteristicas: ['Juguetona', 'Cariñosa', 'Le gusta correr']
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
