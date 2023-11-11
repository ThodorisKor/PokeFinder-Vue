<script setup>
import { ref } from 'vue'

defineProps({
  msg: String,
})

</script>

<template>
 <div class="justify-content-center mt-4">
    <div class="card insidecard ">
      <slot />
    </div>
 </div>
</template>

<style>
.insidcar {
  width: "18rem"
}
</style>
