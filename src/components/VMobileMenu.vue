<template>
  <nav class="navigation">
    <v-icon icon-id="icon-bars" width="22" height="14" />
  </nav>
</template>

<script setup>
import VIcon from '@/components/VIcon.vue'
</script>

<style lang="scss" scoped>
@import '@/assets/variables.scss';

.navigation {
  &:hover {
    cursor: pointer;
  }
}
</style>
