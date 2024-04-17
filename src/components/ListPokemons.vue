<script setup>
const pokemon = defineProps(["name", "urlBaseSvg"])

</script>

<template>
    <div class="col-4">
        <div class="card p-2 mb-3 cardListPokemon">
            <p class="text-center">{{ pokemon.name}}</p>
            <img 
            :src="urlBaseSvg" class="card-img-top" 
            alt="..."
            height="80"
            />
        </div>
    </div>
</template>

<style scoped>
 .cardListPokemon{
    background: rgb(252,186,70);
    background: radial-gradient(circle, rgba(252,186,70,1) 0%, rgba(251,236,63,1) 100%);
    cursor: pointer;
 }

 .cardListPokemon:hover{
    background: rgb(252,186,70);
    background: radial-gradient(circle, rgba(252,186,70,0.6) 0%, rgba(251,236,63,0.4) 100%);
    cursor: pointer;
 }

 .cardListPokemon img:hover{
    padding: .1rem;
 }
</style>