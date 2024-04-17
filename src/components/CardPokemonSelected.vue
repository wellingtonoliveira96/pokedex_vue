<script setup>
const pokemon = defineProps(["name", "xp", "height", "img", "loading"])
</script>

<template>
    <div 
        class="card CardPokemonSelected"
        :class="loading ? '' : 'animate__animated animate__flipInY'"
    >
        <img 
        v-if="pokemon.name"
        :src="pokemon.img" 
        height="250"
        class="card-img-top pt-2" 
        :alt="pokemon.name"
        >
        <img 
        v-else
        src="../assets/egg_pokemon.svg" 
        height="250"
        class="card-img-top pt-2" 
        alt="???"
        >
        <div class="card-body">
            <h5 class="card-title text-center">{{ pokemon.name || '???' }}</h5>
            <hr>
            <div class="row">
                <section class="col">
                    <strong>XP:</strong>
                    <span>{{  pokemon.xp }}</span>
                </section>
                <section class="col">
                    <strong>XP:</strong>
                    <span> {{ pokemon.height }}</span>
                </section>
            </div>
        </div>
    </div>

</template>

<style scoped>
.CardPokemonSelected{
    height: 75vh;
    background: rgb(252,186,70);
    background: radial-gradient(circle, rgb(16, 69, 214) 0%, rgb(30, 163, 216) 100%);
}
</style>