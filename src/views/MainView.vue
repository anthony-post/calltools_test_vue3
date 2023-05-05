<template>
  <div>
    <the-header />
    <section class="data-statistic">
      <h2 class="title title__text">
        Центральная россия — <span class="title__text-black">1/3 экономики страны</span>
      </h2>
      <v-statistic />
    </section>
    <section class="table-map">
      <div class="indicators">
        <v-table />
      </div>
      <div class="map-wrp">
        <img class="map" src="@/assets/images/map.png" alt="map" />
      </div>
    </section>
  </div>
</template>

<script setup>
import TheHeader from '@/components/TheHeader.vue'
import VStatistic from '@/components/VStatistic.vue'
import VTable from '@/components/VTable.vue'
</script>

<style lang="scss" scoped>
@import '@/assets/variables.scss';

.title {
  font-family: $font;
  font-style: normal;
  font-weight: 700;
  font-size: 48px;
  line-height: 60px;

  @media #{$media} and (min-width: $mobile-min) and (max-width: $mobile-max) {
    font-size: 28px;
    line-height: 35px;
  }

  &__text {
    color: $color-main;
    padding: 32px 0;

    @media #{$media} and (min-width: $mobile-min) and (max-width: $mobile-max) {
      color: $color-black;
      padding: 16px 0;
    }
  }

  &__text-black {
    color: $color-black;

    @media #{$media} and (min-width: $mobile-min) and (max-width: $mobile-max) {
      color: $color-main;
    }
  }
}

.data-statistic {
  padding: 0 32px;

  @media #{$media} and (min-width: $mobile-min) and (max-width: $mobile-max) {
    padding: 0 43px 0 16px;
  }
}

.table-map {
  display: flex;
  justify-content: space-between;

  @media #{$media} and (min-width: $mobile-min) and (max-width: $mobile-max) {
    flex-direction: column;
  }
}

.indicators {
  @media #{$media} and (min-width: $mobile-min) and (max-width: $mobile-max) {
    display: none;
  }
}

.map-wrp {
  padding-right: 32px;
  padding-bottom: 16px;

  @media #{$media} and (min-width: $mobile-min) and (max-width: $mobile-max) {
    padding: 33px 46px 20px 16px;
  }
}

.map {
  max-width: 100%;
}
</style>
