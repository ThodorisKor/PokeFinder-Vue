<script setup>
const props = defineProps({
    Pokemon: {
        type:Object
    }
});
</script>

<template>
    <section class="grid justify-center pt-10"> 
        <div class="max-w-sm bg-white border border-gray-200 rounded-lg shadow dark:bg-sky-950 dark:border-gray-700" v-if="(props.Pokemon.photo !== '')">
            <img class="rounded-t-lg m-auto" :src="props.Pokemon.photo" alt="" />
            <div class="p-5">
                <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
                    {{props.Pokemon.label}}
                </h5>
                <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
                    <h3 class="mt-5 mb-2">Abilities :</h3>
                    <ul>
                        <li v-for="ability in props.Pokemon.ability">
                            {{ ability }}
                        </li>
                    </ul>
                </p>
            </div>
        </div>
    </section>
    <!-- <section class="grid grid-flow-col justify-between">
        <div class="max-w-sm bg-white border border-gray-200 rounded-lg shadow dark:bg-sky-950 dark:border-gray-700">
            <img class="rounded-t-lg" src="" alt="" />
            <div class="p-5">
                <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
                    Noteworthy technology acquisitions 2021
                </h5>
                <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
                    Here are the biggest enterprise technology acquisitions of 2021 so far,
                    in reverse chronological order.
                </p>
            </div>
        </div><div class="max-w-sm bg-white border border-gray-200 rounded-lg shadow dark:bg-sky-950 dark:border-gray-700">
            <img class="rounded-t-lg" src="" alt="" />
            <div class="p-5">
                <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
                    Noteworthy technology acquisitions 2021
                </h5>
                <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
                    Here are the biggest enterprise technology acquisitions of 2021 so far,
                    in reverse chronological order.
                </p>
            </div>
        </div>
    </section> -->
</template>

<style></style>
