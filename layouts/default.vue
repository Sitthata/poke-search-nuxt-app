<template>
  <div>
    <section>
      <header class="container mx-auto">
        <nav class="flex justify-between items-center">
          <h1 class="text-2xl font-bold">PokeSearch</h1>
          <ul class="flex gap-4">
            <li><NuxtLink to="/">Home</NuxtLink></li>
            <li><NuxtLink to="/about">About</NuxtLink></li>
          </ul>
        </nav>
      </header>
      <div>
        <slot />
      </div>
    </section>
  </div>
</template>

<script setup lang="ts"></script>
