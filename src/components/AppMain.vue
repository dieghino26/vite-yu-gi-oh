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

}
</style>

