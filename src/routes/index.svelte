<script>
import {pokemon} from "../stores/pokemart";
import PokemanCard from "../components/pokemanCard.svelte"
console.log($pokemon)
</script>

<svelte:head>   
    <title> Home </title>
</svelte:head>
<h1>SvelteKit pokedexzada</h1>
<div>
    {#each $pokemon as pokeman}
    <PokemanCard pokeman = {pokeman}/>
{/each}
</div>