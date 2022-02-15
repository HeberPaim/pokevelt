<script>
    export let pokeman;
</script>
{pokeman.name}
<a href={`/pokeman/${pokeman.id}`}>
    <img src={pokeman.image} alt={pokeman.name}>
    <h2>#{pokeman.id}:  {pokeman.name}</h2>
</a>