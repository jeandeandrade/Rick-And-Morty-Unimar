<template>
  <div class="col-md-4">
    <div class="card mb-3">
      <img :src="image" class="card-img-top" alt="" />
      <div class="card-body">
        <p class="card-title">Nome: {{ char.name }}</p>
        <p class="card-title">Status: {{ char.status }}</p>
        <p class="card-title">Espécie: {{ char.species }}</p>
        <p class="card-title">Gênero: {{ char.gender }}</p>
        <p class="card-title">Localização: {{ char.location.name }}</p>
        <p class="card-title">
          Apareceu em {{ char.episode.length }} episódios
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { defineProps, onMounted, ref } from "vue";
const char = defineProps([
  "name",
  "status",
  "species",
  "gender",
  "location",
  "image",
  "episode",
]);

console.log(char);
</script>

<style></style>
