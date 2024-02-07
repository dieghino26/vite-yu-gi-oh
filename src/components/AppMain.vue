<script>
import PokemonList from './PokemonList.vue';
export default {
    name: "AppMain",
    components: { PokemonList }
}

</script>

<template>
    <main class="container">
        <PokemonList />
    </main>
</template>

<style lang="scss" scoped>
.container {
    background-color: grey;
    border: 10px solid white;
    border-radius: 20px;
    max-width: 1000px;
    max-height: 600px;
    overflow: auto;

}
</style>

