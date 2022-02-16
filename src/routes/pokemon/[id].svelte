<script context="module">
    export async function load({fetch, params})  {
        console.log('loadzada');
        const response = await fetch(`https://pokeapi.co/api/v2/pokemon/${params.id}`);
        const data = await response.json();
        console.log('batatao');
        console.log(data);
        return {
            props: { data }
            }
        }
</script>
<script>
    import { object_without_properties } from "svelte/internal";
    export let data;
    let type = data.types[0].type.name;
</script>
<svelte:head>
	<title>Pokedex - {data.name}</title>
</svelte:head>

<div class="flex flex-col items-center">

    <h1 class="text-4xl text-center my-8 uppercase">{data.name}</h1>
    <img class="card-image animate-spin" alt={data.name} src={data.sprites.other['official-artwork']['front_default']}>
    <p>
        Type: <span class ="rounded-sm p-1 border-2 text-xs border-slate-500/50 {type}"> {type.toUpperCase()}</span> 
        {#if (typeof data.types[1] != 'undefined')}
        <span class ="rounded-sm p-1 border-2 text-xs border-slate-500/50 {data.types[1].type.name}"> {data.types[1].type.name.toUpperCase()}</span> 
        {/if}
        | Height: <strong>{data.height}</strong> | Weight: <strong>{data.weight}</strong>
    </p>
</div>

<style>
    .normal{
        background-color:#aa9;
    }
    .fire{
        background-color:#f42;
    }
    .water{
        background-color:#39f;
    }
    .electric{
        background-color:#fc3;
    }
    .grass{
        background-color:#7c5;
    }
    .ice{
        background-color:#6cf;
    }
    .fighting{
        background-color:#b54;
    }
    .poison{
        background-color:#a59;
    }
    .ground{
        background-color:#db5;
    }
    .flying{
        background-color:#89f;
    }
    .psychic{
        background-color:#f59;
    }
    .bug{
        background-color:#ab2;
    }
    .rock{
        background-color:#ba6;
    }
    .ghost{
        background-color:#66b;
    }
    .dragon{
        background-color:#76e;
    }
    .dark{
        background-color:#754;
    }
    .steel{
        background-color:#aab;
    }
    .fairy{
        background-color:#e9e;
    }
</style>