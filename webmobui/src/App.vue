<script setup>
import { computed, ref } from "vue";

const baseK = ref(0);

const Cvalue = computed(() => {
  return baseK.value - 273.15;
});

const Fvalue = computed(() => {
  return baseK.value * 1.8 - 459.67;
});

const updateValue = (event) => {
  baseK.value = event.target.value;
};
</script>




<template>
  <label>Base </label>
  <input type="number" :value = "baseK" @input="updateValue($event)"/>
  <label>Celsius </label>
  <input type="number" :value = "Cvalue" />
  <label >Farenheit </label>
  <input type="number" :value = "Fvalue" />
</template>
