<template>
  <header class="header header__wrp">
    <RouterLink to="/" class="logo">
      <img alt="logo" class="logo" src="@/assets/logo.svg" width="111" height="14" />
    </RouterLink>
    <v-mobile-menu />
  </header>
</template>

<script setup>
import VMobileMenu from '@/components/VMobileMenu.vue'
</script>

<style lang="scss" scoped>
@import '@/assets/variables.scss';
.header {
  box-shadow: 0px 0px 1px rgba(9, 30, 66, 0.31), 0px 4px 8px rgba(9, 30, 66, 0.25);
}

.header__wrp {
  display: flex;
  justify-content: space-between;
  padding: 21px 32px;

  @media #{$media} and (min-width: $mobile-min) and (max-width: $mobile-max) {
    padding: 21px 16px;
  }
}
</style>
