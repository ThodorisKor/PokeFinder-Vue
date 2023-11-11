<script setup>
import { ref } from 'vue'
import axios from 'axios';


defineProps({
  msg: String,
})

const count = ref(0)
</script>

<template>
  <div class="text-center mb-5 mt-5 text-warning">
    <h1>Poké Finder</h1>
  </div>
  
  <form
    class="d-flex justify-content-center mt-4"
  >
    <div className="form-floating">
      <input
        placeholder="Enter Username"
        id="pokemon"
        type="text"
        name="pokemon"
        class="form-control"
        @click={changeHandler}
      />

      <label htmlFor="Search Pokemon">Search Pokemon</label>
    
      </div>
      <div>
        <button
          id="search"
          type="submit"
          class="btn btn-primary h-100 btn-rip"
        >
          <i class="fa fa-search"></i>
        </button>
      </div>

  </form>
</template>

<style>

</style>
