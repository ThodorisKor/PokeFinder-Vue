<script setup>
import { ref } from 'vue'
import Card from './Card.vue';
defineProps({
  msg: String,
})

const count = ref(0)
</script>

<template>
   <Card>
      <img
        className="card-img-top"
        id="photo"
        src={props.Pokemon.photo}
        alt="Card"
      />
      <div className="card-body">
        <h5 id="label" className="card-title">
          {props.Pokemon.label}
        </h5>
        <p>
          weight : <span id="weight">{props.Pokemon.weight}</span>
        </p>
        <h6>Abilities :</h6>
       
      </div>
    </Card>
</template>

<style scoped>
.insidcar {
  width: "18rem"
}
</style>
