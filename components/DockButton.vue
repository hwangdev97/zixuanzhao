<script lang="ts" setup>
defineProps<{
  dockLinkItem: DockLinkItem
}>()
</script>

<template>
  <div class="item border bg-white dark:border-black dark:bg-black">
    <NuxtLink :to="dockLinkItem.route">
      <div :class="dockLinkItem.icon" />
    </NuxtLink>
  </div>
</template>

<style scoped>
.item {
  width: 100%;
  height: 100%;
  min-height: 60px;
  min-width: 60px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
}
</style>
