<script setup>
import characterList from '@/components/characterList.vue'
import { onMounted, reactive, ref } from 'vue';

let characters = reactive(ref())

onMounted(() => {
  fetch("https://rickandmortyapi.com/api/character/?page=2")
    .then(response => response.json())
    .then(response => {
      characters.value = response.results
      console.log(character)
    })
})
 
</script>

<template>
  <h1 class="title" style="text-align: center; margin-top: 1rem;">Personagens</h1>
  <main style="padding: 1rem 4rem 3rem;">
      <div class="row row-cols-3">
            <characterList v-for="character in characters"
            :key="character.id"
            :name="character.name"
            :image="character.image"
            :status="character.status"
            :species="character.species"
            :gender="character.gender"
            :location="character.location"
            :episodes="character.episode"/>
    </div>
  </main>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@200..700&display=swap');

h1{
  color: #00ff40;
  font-family: 'Oswald';
}
</style>

