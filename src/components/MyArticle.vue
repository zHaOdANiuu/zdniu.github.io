<script setup lang="ts">
const data = ['2025']
</script>

<template>
  <section
    style="--line-left: 47.5%"
    class="left-12 grid grid-cols-[10%_75%] line-before"
  >
    <div style="--line-left: 0%" class="times line-before">
      <time
        class="line-point hover:text-[var(--n-line-text-hover)]"
        v-for="(v, i) in data"
        :key="i"
        >{{ v }}</time
      >
    </div>
    <div>
      <h1 class="text-2xl font-light"></h1>
    </div>
  </section>
</template>

<style lang="css">
@reference 'tailwindcss';

.line-before {
  --line-left: 0%;
  @apply relative;
}
.line-before::before {
  @apply absolute content-[''] top-0 bottom-0 left-[var(--line-left)] border-l-2 border-[var(--n-line)];
}
.line-point {
  --text-offset: 10px;
  @apply relative block text-2xl font-light pt-6 pl-[var(--text-offset)];
}
.line-point::before {
  @apply absolute
    content-['']
    top-1/2
    left-0
    size-2
    rounded-[50%]
    ml-[var(--text-offset)]
    bg-[var(--n-line-point)]
    transform-[translate(-50%,100%)];
}
</style>
