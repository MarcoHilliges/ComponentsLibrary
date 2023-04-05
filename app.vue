<template>
    <NuxtLoadingIndicator />
    <div class="bg-gray-800 h-screen p-6">
      <NavigationBarSimple />
      <NuxtPage />
    </div>
</template>

<script setup lang="ts">
const route = useRoute()
</script>

<style lang="scss" scoped>

</style>