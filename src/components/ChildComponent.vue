<template >
<h2>--</h2>
  <div>
    <h3>Producto</h3>
    <p>Id: {{ product.id }}</p>
    <p>Nombre: {{ product.name }}</p>
    <p>Precio: {{ product.price }}</p>
  </div>
</template>

<script setup>

const props = defineProps({
  product: {
    type: Object,
    required: true
  }
})
</script>