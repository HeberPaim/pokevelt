<script>
import {pokemon} from "../stores/pokemart";
import PokemanCard from "../components/pokemanCard.svelte"
console.log($pokemon)
</script>

<svelte:head>   
    <title> Pokedex </title>
</svelte:head>

<h1 class="text-white text-4xl text-center my-8 ">Svelte Kit Pokedexzada</h1>
<div class="py-4 grid gap-4 lg:grid-cols-3 md:grid-cols-2 sm:grid-cols-1">
    {#each $pokemon as pokeman}
        <PokemanCard pokeman = {pokeman}/>
    {/each}
</div>