<script setup lang="ts">
const online = useOnline()
</script>

<template>
  <!-- <Logos mb-6 />
    <Suspense>
      <ClientOnly>
        <PageView v-if="online" />
        <div v-else text-gray:80>
          You're offline
        </div>
      </ClientOnly>
      <template #fallback>
        <div italic op50>
          <span animate-pulse>Loading...</span>
        </div>
      </template>
    </Suspense>
    <InputEntry /> -->
  <SectionHome class="h-full w-full" />
</template>
