<template>

<nav class="border-gray-200 bg-gray-50 dark:bg-gray-800 dark:border-gray-700">
  <div class="max-w-screen-lg flex flex-wrap items-center justify-between mx-auto p-4">
    <NuxtLink to="#" class="flex items-center space-x-2">
        <figure class="h-16 w-16 rounded-lg bg-gray-300">
        	<img src="https://www.unsplash.com/16/16" />
        </figure>
        <span class="self-center text-2xl font-semibold whitespace-nowrap dark:text-white">sallmaxo</span>
    </NuxtLink>
    <button type="button" class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600">
        <span class="sr-only">Open main menu</span>
        <svg class="w-5 h-5" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 17 14">
            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 1h15M1 7h15M1 13h15"/>
        </svg>
    </button>
    <div class="hidden w-full md:block md:w-auto" id="navbar-solid-bg">
      <ul class="w-full flex flex-col font-normal text-sm p-4 md:p-0 mt-4 rounded-md bg-white md:flex-row md:items-center md:mt-0 md:border-0 md:bg-white dark:bg-gray-800 md:dark:bg-gray-900 dark:border-gray-700">
        
        <li v-for="link in links">
          <NuxtLink :to="link.href" :key="link.href" 
          :class="[link.href === $route.path 
          	? 'bg-sky-100 text-black font-medium'
          	: 'bg-sky-600', 'block text-white py-2 pl-3 pr-4 text-gray-900 hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:px-4 md:py-2 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent transition-all hover:transition-all active:transition-all']">{{ link.label }}</NuxtLink>
        </li>
       
      </ul>
    </div>
  </div>
</nav>

</template>

<script setup>
	const route = useRoute()
	const links = [
		{'label':'home', 'href':'/'},
		{'label':'about ','href':'/about'},
		{'label':'features', 'href':'/features'},
		{'label':'purches', 'href':'/purches'},
		{'label':'contact', 'href':'/contact-us'},
	]
</script>
<style scoped>
	.navbar-item{
		@apply block text-white py-2 pl-3 pr-4 text-gray-900 hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:px-4 md:py-2 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent transition-all hover:transition-all active:transition-all 
	}
</style>

