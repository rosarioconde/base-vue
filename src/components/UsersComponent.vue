<template>

    <h1>User List</h1>
    <ul>
        <li v-for="user in users" :key="user.id">
         {{user.id }} -  {{ user.name }} - {{ user.email }} -{{ user.phone }}
        </li>
    </ul>
</template>

<script setup>
import { ref, onMounted } from 'vue'

const users = ref([])
const fetchUsers = async () => {
  const response = await fetch('https://jsonplaceholder.typicode.com/users')
  users.value = await response.json()  
}

onMounted(fetchUsers)

</script>

<!-- <template>
  <div>
    <p>{{ message }}</p>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';

// Definir una variable reactiva para el mensaje
const message = ref('');

// Usar onMounted para actualizar el mensaje después de que el componente se monta
onMounted(() => {
  message.value = 'El componente ha sido montado en el DOM!';
});
</script> -->




