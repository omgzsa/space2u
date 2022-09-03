<script setup>
import TheContactItem from './TheContactItem.vue';

const props = defineProps({
  address: String,
  email: String,
  mapsLink: String,
});
</script>

<template>
  <div>
    <TheContactItem>
      <template #title> iroda </template>
      <template #value>
        <a class="font-regular" :href="`${props.mapsLink}`" target="_blank">
          {{ props.address }}</a
        >
      </template>
    </TheContactItem>
    <TheContactItem>
      <template #title> kapcsolat </template>
      <template #value>
        <a class="font-regular" href="mailto:hello@space2u.hu">
          {{ props.email }}</a
        >
      </template>
    </TheContactItem>
  </div>
</template>

<style></style>
