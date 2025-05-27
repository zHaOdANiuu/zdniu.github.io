<template>
  <div class="relative top-8 flex flex-col gap-8">
    <WebItem
      v-for="(props, index) in webList"
      :key="index"
      :width="'240px'"
      :height="'72px'"
      :title="props.title"
      class="text-[18px]"
    >
      <template #default>
        <component :is="props.icon" />
      </template>
    </WebItem>
  </div>
</template>

<script setup lang="ts">
import IconBiliBili from './icon/IconBiliBili.vue'
import IconGitHub from './icon/IconGitHub.vue'
import IconQQ from './icon/IconQQ.vue'
import WebItem from './WebItem.vue'
const webList = [
  {
    title: 'BiliBili',
    icon: IconBiliBili
  },
  {
    title: 'GitHub',
    icon: IconGitHub
  },
  {
    title: 'QQ',
    icon: IconQQ
  }
]
</script>
