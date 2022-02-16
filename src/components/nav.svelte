<script>
    import logo from './srcp/pokecamera.png'
    import Button from './button.svelte'
</script>
<!--     
<nav
 class="flex justify-center w-full">
    <a class="mx-4 text-lg" href="/">Home</a>
    <a class="mx-4 text-lg" href="/about">Sobre</a>


</nav>
-->
<nav class="bg-white border-gray-200 px-2 sm:px-4 py-2.5 w-full rounded dark:bg-gray-800">
    <div class="container flex flex-wrap justify-between items-center mx-auto">
      <a href="/" class="flex">
        <img src={logo} class = "mr-3 h-10" alt="pokedex">
          <span class="self-center text-lg font-semibold whitespace-nowrap dark:text-white"></span>
      </a>
      <button data-collapse-toggle="mobile-menu" type="button" class="inline-flex items-center p-2 ml-3 text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600" aria-controls="mobile-menu-2" aria-expanded="false">
        <span class="sr-only">Open main menu</span> </button>
      <div class="hidden w-full md:block md:w-auto" id="mobile-menu">
        <ul class="flex flex-col mt-4 md:flex-row md:space-x-8 md:mt-0 md:text-sm md:font-medium">
          <li>
            <a href="/" class="block py-2 pr-4 pl-3 text-white bg-blue-700 rounded md:bg-transparent md:text-blue-700 md:p-0 dark:text-white" aria-current="page">Home</a>
          </li>
          <li>
            <a href="/" class="block py-2 pr-4 pl-3 text-gray-700 border-b border-gray-100 hover:bg-gray-50 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 dark:text-gray-400 md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent dark:border-gray-700">About</a>
          </li>
            <li>
                <Button>
                    Dark Mode?
                </Button>
            </li>
        </ul>
      </div>
    </div>
  </nav>

<style>
	:global(body) {
		background-color: #f2eee2;
		color: black;
		transition: background-color 0.3s;
	}
	:global(body.dark-mode) {
		background-color: #1d3040;
		color: #bfc2c7;
	}
</style>