<script setup></script>

<template>
  <div class="d-flex">
    <span class="font-bold uppercase contact-title">
      <slot name="title" />
    </span>

    <span class="contact-value">
      <slot name="value" />
    </span>
  </div>
</template>

<style scoped>
.contact-title:after {
  content: '/';
  color: var(--sp-red);
  padding-right: 0.25em;
  font-weight: 700;
}
</style>
