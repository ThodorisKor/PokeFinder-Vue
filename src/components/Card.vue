<script setup>
import { ref } from 'vue'

defineProps({
  msg: String,
})

const count = ref(0)
</script>

<template>
 <div class="row justify-content-center mt-4">
    <div class="card insidecard">

    </div>
 </div>
</template>

<style scoped>
.insidcar {
  width: "18rem"
}
</style>
