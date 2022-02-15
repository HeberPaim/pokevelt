<script>
    export let pokeman;
</script>
<a class="p-6 bg-gray-100 text-gray-800 text-center rounded-md shadow-sm flex flex-col items-center" href={`/pokeman/${pokeman.id}`}>
    <img class="animate-bounce" src={pokeman.image} alt={pokeman.name}>
    <h2>#{pokeman.id}:  {pokeman.name}</h2>
</a>

