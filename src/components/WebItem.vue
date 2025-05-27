<template>
  <div
    class="flex justify-between items-center rounded-2xl p-3 bg-[var(--n-web-list)]"
    :style="{ width, height }"
  >
    <span>{{ title }}</span>
    <slot></slot>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  title: string
  width: string
  height: string
}>()
</script>
