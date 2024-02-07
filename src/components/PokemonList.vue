<script>
import axios from "axios";
const endpoint = "https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons"
export default {
    name: "PokemonList",
    data: () => ({
        pokemons: []
    }),
    created() {
        axios.get(endpoint).then(res => {
            this.pokemons = res.data.docs;
        })
    }
};
</script>

<template>
    <div id="pokemon" class="row">
        <div class="col my-3 mx-2" v-for="pokemon in pokemons">
            <img :src="pokemon.imageUrl" alt="">
            <div>{{ pokemon.number }}</div>
            <div>{{ pokemon.name }}</div>
            <div class="type">{{ pokemon.type1 }}</div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
#pokemon {
    display: flex;
    flex-wrap: wrap;

    .col {
        background-color: white;
        border-radius: 20px;
        text-align: center;
        font-weight: bold;
        padding: 5px;
    }

    img {
        height: 150px;
        width: 150px;
        border-radius: 20px;
    }

}
</style>