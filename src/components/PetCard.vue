<template>
  <div v-if="mascota">
    <h2>{{ mascota.nombre }}</h2>
    <p>Tipo: {{ mascota.tipo }}</p>
    <p>Edad: {{ mascota.edad }} años</p>

    <p v-if="mascota.vacunado">Vacunado: Sí</p>
    <p v-else>Vacunado: No</p>

    <img :src="mascota.foto" :alt="mascota.nombre" />

    <h3>Características</h3>
    <ul>
      <li v-for="(caracteristica, index) in mascota.caracteristicas" :key="index">
        {{ caracteristica }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'PetCard',
  props: {
    mascota: {
      type: Object,
      required: true
    }
  }
}
</script>
