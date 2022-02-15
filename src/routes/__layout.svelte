<script>
	import Nav from "../components/nav.svelte"
</script>
<div class="bg-gradient-to-r from-indigo-900 via-purple-500 to-pink-500">
	<div class=" p-8 max-w-6xl mx-auto">
		<Nav/>
		<slot>
		</slot>
	</div>
</div>
	<style>
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
</style>