<script>
    export let pokeman;
</script>
<a id = "poketype"class="p-6 bg-gray-100 text-gray-800 text-center rounded-md shadow-sm flex flex-col items-center " href={`/pokemon/${pokeman.id}`}>
    <img  class="animate-bounce" src={pokeman.image} alt={pokeman.name}>
    <h2>#{pokeman.id}:  {pokeman.name}</h2>
</a>
<style>
    a{
        background: linear-gradient(35deg, rgba(165, 253, 253, 0.65) , rgba(255, 176, 176, 0.65));
        
    }
    :global(h2.dark-mode){
        background-color: indigo;
    }
    #poketype h2{
        color:black;
    }
</style>