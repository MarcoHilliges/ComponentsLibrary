<template>
    <NuxtLoadingIndicator />
    <div class="flex bg-gray-800 h-screen">
      <div class="w-48">
        <NuxtLink to="/" class="h-24 flex items-center justify-center">
          <img class="h-16" src="@/assets/Logo-dark.png" alt="Logo">
        </NuxtLink>
        <NavigationBarSimple />
      </div>
      <div>
        <header class="h-[50px]">
          
        </header>
        <main class="w-[calc(100vw-200px)] h-[calc(100vh-100px)] overflow-auto bg-gray-700">
          <NuxtPage />
        </main>
        <footer>

        </footer>
      </div>
      
    </div>
</template>

<script setup lang="ts">
const route = useRoute()
</script>

<style lang="scss" scoped>

</style>