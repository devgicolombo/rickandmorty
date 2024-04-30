<script setup>

import { onMounted, reactive, ref } from 'vue';
import ListPersonagens from '../components/ListPersonagens.vue';

let personagens = reactive(ref())


onMounted(() => {
  fetch("https://rickandmortyapi.com/api/character")
  .then(response => response.json())
  .then(response => {
    personagens.value = response.results
    console.log(personagens)
  })
})
</script>


<template>
<body>
  <section>
  <main>
    <div class="container">
      <img src="https://upload.wikimedia.org/wikipedia/commons/b/b1/Rick_and_Morty.svg" alt="" style="width: 100%; max-width: 100%; max-height: 100%;">
      <ListPersonagens 
    v-for="personagem in personagens"
    :key="personagem.name"
    :name="personagem.name"
    :url="personagem.url"
    :image="personagem.image"
    :status="personagem.status"
    :species="personagem.species"
    :gender="personagem.gender"
    :location="personagem.location"
    :episode="personagem.episode"
    :style="{ color: 'black', fontSize: '20px' }" 
>
    {{ personagem.name }}
</ListPersonagens>
    </div>
  </main>
</section>
</body>
</template>

<style>

.container{
  display: flex;
  flex-wrap: wrap;
}

</style>

