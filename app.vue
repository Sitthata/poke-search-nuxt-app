<template>
  <div>
    <h1 class="text-4xl font-bold">Welcome to the home page</h1>
    <Button @click="count++">Count: {{ count }}</Button>
  </div>
</template>

<script setup lang="ts">
const count = ref<number>(0) ;
</script>
