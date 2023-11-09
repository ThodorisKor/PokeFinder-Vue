<script setup>
import { ref } from 'vue'

defineProps({
  msg: String,
})

const count = ref(0)
</script>

<template>
    <div clas="container contain">
        <div class="row mt-4 justify-content-center">{props.children}</div>
    </div>
</template>

<style scoped>

</style>
