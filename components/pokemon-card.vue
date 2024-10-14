<template>
  <div>
    <div class="flex justify-center">
      <Input v-model="pokemonName" type="text" placeholder="Pokemon name" />
      <Button>Search</Button>
    </div>

    <div v-if="pokemon">
      <NuxtImg :src="pokemon?.sprites?.front_default" />
    </div>
  </div>
</template>

<script setup lang="ts">
interface Pokemon {
  name: string;
  sprites: {
    front_default: string;
  };
}
const pokemonName = ref<string>("");

function searchPokemon() {
  $fetch<Pokemon>(`https://pokeapi.co/api/v2/pokemon/${pokemonName.value}`, {
    method: "GET",
  });
}


</script>
