<template>
    <div class="detail-card">
      <h2>Pokemon Details</h2>
      <div>
        <p><strong>Name:</strong> {{ pokemonData.name }}</p>
        <p><strong>Height:</strong> {{ pokemonData.height }}</p>
        <p><strong>Weight:</strong> {{ pokemonData.weight }}</p>
        <p><strong>Abilities:</strong></p>
        <ul>
          <li v-for="ability in pokemonData.abilities" :key="ability.ability.name">
            {{ ability.ability.name }}
          </li>
        </ul>
        <!-- Add more properties as needed -->
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      pokemonData: {
        type: Object,
        required: true
      }
    }
  };
  </script>
  
  <style scoped>
  .detail-card {
    border: 1px solid #ccc;
    padding: 10px;
    margin-top: 20px;
  }
  </style>