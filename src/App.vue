<script setup lang="ts">
import { ref } from 'vue';
import SizeSelector from './components/SizeSelector.vue';

const selectedSize = ref<String>('M');

</script>

<template>
 <h1>Seleccione la talla: {{selectedSize}} </h1>
 <SizeSelector
 :selected-size="selectedSize"
 @on-changed-size="selectedSize = $event"
 
 />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
button{
  padding: 5px;
  margin: 5px;
  border: none;
  border-radius: 5px;
  width: 75px;
  cursor: pointer;

}
.active{
  background-color: black;
  color:white;
  transition: all .3s ease-out ;

}
</style>
