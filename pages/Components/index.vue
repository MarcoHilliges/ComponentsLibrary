<template>
    <div>
      <button @click="showButtons = 'metalButtons'">
        Metal-Buttons
      </button>

      {{ showButtons }}

      <div v-if="showButtons === 'metalButtons'">
        huhu
        <ButtonsMetalicButton />
      </div>
        
    </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  setup() {
    const showButtons = ref('');
    return { showButtons };
  },
});
</script>

<style scoped>

</style>