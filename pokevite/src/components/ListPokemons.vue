<script setup>

const pokemon = defineProps(["name", "urlBaseSVG"])

</script>

<template>
  
<div class="col-4">
    <div class="card p-2 mb-3 cardListPokemon">
        <p class="text-center">{{ pokemon.name }}</p>
        <img :src="urlBaseSVG" class="card-img-top" alt="..." height="80">
    </div>
</div>

</template>

<style scoped>
.cardListPokemon{
    background: rgb(238,174,202);
    background: radial-gradient(circle, rgba(238,174,202,1) 0%, rgba(148,187,233,1) 100%);
    cursor: pointer;
}

.cardListPokemon:hover{
    background: rgb(238,174,174);
    background: radial-gradient(circle, rgba(238,174,174,1) 0%, rgba(148,233,205,1) 100%);
    cursor: pointer;
}

.cardListPokemon img:hover{
    padding: .1rem;
}

</style>