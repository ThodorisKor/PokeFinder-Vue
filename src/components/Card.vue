<script setup>
import { ref } from 'vue'

defineProps({
  msg: String,
})

</script>

<template>
 <div class="row justify-content-center mt-4">
    <div class="card insidecard">
      {{ msg }}
    </div>
 </div>
</template>

<style scoped>
.insidcar {
  width: "18rem"
}
</style>
