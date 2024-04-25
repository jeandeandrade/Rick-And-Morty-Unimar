<template>
  <main>
    <div class="container">
      <div class="card mb-3" style="max-width: 1000px">
        <div class="row g-0">
          <div class="col-md-4 character-card">
          </div>
          <div class="col-md-12">
            <div class="card characters-list-card">
              <div class="card-body row">
                <ListCharacters
                  v-for="character in characters"
                  :key="character.name"
                  :image="character.image"
                  :name="character.name"
                  :status="character.status"
                  :species="character.species"
                  :gender="character.gender"
                  :location="character.location"
                  :episode="character.episode"
                />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<script setup>
import { onMounted, reactive, ref } from "vue";
import ListCharacters from "../components/ListCharacters.vue";

let characters = reactive(ref());

onMounted(() => {
  fetch("https://rickandmortyapi.com/api/character/?page=1")
    .then((response) => response.json())
    .then((response) => {
      characters.value = response.results;
      console.log(characters);
    });
});
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Acme");

main {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background: radial-gradient(#156f99, #0a2e50);
  font-family: "Acme", sans-serif;
}

.container {
  display: flex;
  justify-content: center;
  margin-top: 150px;
}

.card {
  background-color: #fff;
  border-radius: 10px;
  box-shadow: 0px 0px 15px 0px rgba(0, 0, 0, 0.1);
}

.card-body {
  padding: 20px;
}

.characters-list-card {
  padding: 20px;
}
</style>
