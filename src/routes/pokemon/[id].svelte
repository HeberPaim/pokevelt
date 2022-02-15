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
    export let data;
    const type = data.types[0].type.name;
</script>
<svelte:head>
	<title>Pokedex - {data.name}</title>
</svelte:head>

<div class="flex flex-col items-center">

    <h1 class="text-4xl text-center my-8 uppercase">{data.name}</h1>
    <p>Type: <strong>{type}</strong> | Height: <strong>{data.height}</strong>
        | Weight: <strong>{data.weight}</strong>
    </p>
    <img class="card-image" src={data.sprites['front_default']} 
    alt={data.name}
    />
</div>