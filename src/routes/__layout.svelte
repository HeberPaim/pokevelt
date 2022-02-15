<script>
	import "fluent-svelte/theme.css";
</script>
<nav>
	<a href="/">Home</a>
	<a href="/about">About</a>
	<a href="/settings">Settings</a>
</nav>

<slot></slot>

<style>
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
</style>