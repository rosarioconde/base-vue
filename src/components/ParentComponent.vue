<template>
<div>
  <h1>Componente padre</h1>
  <ChildComponent :product="product" />
  <ChildComponent :product="{id: 2, name: 'otra cosa', price: 20}" />
  
</div>
</template>

<script setup>
import { ref } from 'vue'
import ChildComponent from './ChildComponent.vue'

const product = ref({id: 1, name: 'Laptop', price: 1000})
</script>

