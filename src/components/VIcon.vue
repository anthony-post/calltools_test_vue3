<template>
  <svg class="icon" :width="width" :height="height">
    <use :xlink:href="iconPath" />
  </svg>
</template>

<script>
import { computed } from 'vue'
import spriteUrl from '@/assets/sprite.svg'

export default {
  name: 'VIcon',
  props: {
    iconId: {
      type: String,
      required: true
    },
    width: {
      type: [Number, String],
      default: 32
    },
    height: {
      type: [Number, String],
      default: 32
    }
  },
  setup(props) {
    const iconPath = computed(() => {
      return `${spriteUrl}#${props.iconId}`
    })
    return { iconPath }
  }
}
</script>

<style lang="scss">
@import '@/assets/variables.scss';

.icon {
  fill: $color-icon;
}
</style>
