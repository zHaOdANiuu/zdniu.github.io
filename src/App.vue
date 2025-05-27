<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import router from './router'
</script>

<template>
  <header>
    <nav class="base-pink header-nav">
      <RouterLink
        active-class="active"
        v-for="(v, i) in router.options.routes"
        :key="i"
        :to="v.path"
        >{{ v.name }}</RouterLink
      >
    </nav>
  </header>
  <main class="relative">
    <RouterView class="h-full" />
    <img src="/NIU.png" class="absolute inset-0 opacity-15 size-full" />
  </main>
  <footer class="base-pink">
    <div>123</div>
  </footer>
</template>

<style lang="css">
@reference 'tailwindcss';

.base-pink {
  @apply flex justify-start bg-[#faa0d2] pl-10 pt-2 gap-8;
}

.header-nav a {
  @apply h-12 text-[18px] font-light transition-all duration-200;
}

.header-nav a:hover {
  color: #f32e9e;
}

.header-nav a.active {
  font-weight: normal;
  padding-bottom: 4px;
  border-bottom: 2px solid currentColor;
  transform: scale(1.03);
}
</style>
