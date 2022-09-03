<script setup>
defineProps({
  content: String,
});
</script>

<template>
  <div class="mb-4">
    <h3 class="font-bold uppercase grey-light">filozófia</h3>

    <slot />

    <p class="font-bold">
      Megbízók számára magas minőségű, kreatív téralkotás.
    </p>
  </div>
</template>

<style></style>
