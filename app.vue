<template>
    <NuxtLoadingIndicator />
    <div class="flex bg-gray-800 h-screen">
      <div class="w-48">
        <NuxtLink to="/" class="h-24 flex items-center justify-center">
          <img class="h-16 -ml-5" src="@/assets/Logo-dark.png" alt="Logo">
        </NuxtLink>
        <NavigationBarSimple :currentRoute="currentRoute" :avelableRoutes="avelableRoutes" />
      </div>
      <div>
        <header class="h-[50px]">
          
        </header>
        <main class="mainScreen w-[calc(100vw-200px)] h-[calc(100vh-100px)] overflow-auto bg-gray-700">
          <NuxtPage />
        </main>
        <footer>

        </footer>
      </div>
      
    </div>
</template>

<script lang="ts">
import { defineComponent, computed } from 'vue';
import { useRoute } from 'vue-router';

export default defineComponent({
  setup() {
    const route = useRoute();
    const currentRoute = computed(() => route.path);
    const avelableRoutes = [
      {name: 'Home', to: '/'},
      {name: 'Components', to: '/components'},
      {name: 'NuxtOriginal', to: '/nuxtOriginal'}
    ]
    return { currentRoute, avelableRoutes };
  },
});
</script>

<style scoped>
.mainScreen {
}
</style>