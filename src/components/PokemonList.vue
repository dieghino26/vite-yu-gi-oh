<script>
import axios from "axios";
const endpoint = "https://pokeapi.co/api/v2/pokemon"
export default {
    name: "PokemonList",
    data: () => ({
        pokemon: []
    }),
    created() {
        axios.get(endpoint).then(res => {
            this.pokemon = res.data.results;
        })
    }
};
</script>

<template>
    <section id="pokemon">

    </section>
</template>