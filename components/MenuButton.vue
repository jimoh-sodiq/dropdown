<template>
  <OnClickOutside @trigger="closeDropdown">
    <button @click="toggleDropdown">
      <slot />
    </button>
  </OnClickOutside>
</template>

<script setup>
import { OnClickOutside } from "@vueuse/components";

const { toggleDropdown, closeDropdown } = inject("dropdown");
</script>
