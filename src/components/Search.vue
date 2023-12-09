<script setup>
import { ref } from 'vue';

const pokemon = ref();
</script>
<template>
    <section class="flex justify-center">
            <form class="flex-1 max-w-sm" @submit.prevent="$emit('getPokemon',pokemon);">
                <label for="default-search"
                    class="mb-2 text-sm font-medium text-gray-900 sr-only dark:text-white">Search</label>
                <div class="relative">
                    <div class="absolute inset-y-0 start-0 flex items-center ps-3 pointer-events-none">
                        <svg class="w-4 h-4 text-gray-500 dark:text-gray-400" aria-hidden="true"
                            xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 20 20">
                            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="m19 19-4-4m0-7A7 7 0 1 1 1 8a7 7 0 0 1 14 0Z" />
                        </svg>
                    </div>
                    <input v-model="pokemon" type="search" id="default-search" class="block w-full p-4 ps-10 text-sm text-gray-900 border  rounded-lg  focus:ring-sky-500 focus:border-sky-500 dark:bg-gray-700 dark:border-sky-600  dark:text-white dark:focus:ring-sky-500 dark:focus:border-sky-500" required />
                    <button type="submit"
                        class="text-white absolute end-2.5 bottom-2.5 bg-sky-700 hover:bg-sky-800 focus:ring-4 focus:outline-none focus:ring-sky-300 font-medium rounded-lg text-sm px-4 py-2 dark:bg-sky-600 dark:hover:bg-sky-700 dark:focus:ring-sky-800">
                        Search
                    </button>
                </div>
            </form>
        </section>
</template>


<style>
    
</style>