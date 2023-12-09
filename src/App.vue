<script setup>
import Heading from "./components/Heading.vue";
import Search from "./components/Search.vue";
import Card from "./components/Card.vue";
import { reactive, ref } from "vue";
import axios from "axios";
const pokemon = reactive({
    photo: '',
    label: '',
    weight: '',
    ability: [],
});

function GetFormValue(value) {
  //pokemon.value = value;
  axios
    .get(`https://pokeapi.co/api/v2/pokemon/${value}`)
    .then((response) => {
      const abilities = response.data.abilities.map(
        (ability) => ability.ability.name
      );

      // Update the reactive variable with fetched Pokemon data
      pokemon.photo = response.data.sprites.other["official-artwork"].front_default;
      pokemon.label = response.data.name;
      pokemon.weight = response.data.weight;
      pokemon.ability = abilities;
    })
    .catch((error) => {
      console.error("Error fetching Pokemon data:", error);
    });
}
</script>

<template>
  <main class="max-w-6xl mx-auto mt-6 lg:mt-20 space-y-6">
    <Heading />
    <Search @getPokemon="GetFormValue" />
    <Card  :Pokemon="pokemon" v-if="pokemon.photo !== ''"/>
    <section v-else class="flex justify-center">
        <h1 class="text-4xl mt-40  text-zinc-600" >No Pokemons...</h1>
    </section>
  </main>
</template>

<style scoped></style>
