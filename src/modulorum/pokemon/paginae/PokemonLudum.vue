<template>
    <section v-if="estPortat" class="flex flex-col justify-center items-center w-screen h-screen">
        <h1 class="text-3xl">Espere, por favor</h1>
        <h3 class="animate-pulse">Cargando Pokemons</h3>
    </section>

    <section v-else class="flex flex-col justify-center items-center w-screen h-screen">
        <h1 class="m-5">¿Quién es este Pokemon?</h1>

        <Pokemonimago/>
        <PokemonOptiones/>

    </section>
</template>

<script setup lang="ts">
import Pokemonimago from '../components/PokemonImago.vue';
import PokemonOptiones from '../components/PokemonOptiones.vue';
import { usePokemonLudum } from '../composables/usePokemonLudum';

const {estPortat , ludumStatus} = usePokemonLudum();


</script>

<style scoped>

</style>