<template>
  <div class="row">
    <div v-for="dataItem in dataStatistic" :key="dataItem.id" class="col">
      <span class="col__title">{{ dataItem.name }}</span>
      <div class="col-wrp">
        <dl v-for="item in dataItem.data" :key="item.id" class="col__list">
          <dt class="col__value">{{ item.value }}&#37;</dt>
          <dd class="col__item">{{ item.name }}</dd>
        </dl>
      </div>
    </div>
  </div>
</template>

<script setup>
const dataStatistic = [
  {
    id: 1,
    name: 'ДЕНЬГИ',
    data: [
      {
        id: 1,
        name: 'финансовых влияний',
        value: 73
      },
      {
        id: 2,
        name: 'накопленных прямых иностранных инвестиций',
        value: 53
      },
      {
        id: 3,
        name: 'инвестиций в основной капитал',
        value: 29
      }
    ]
  },
  {
    id: 2,
    name: 'ПРОИЗВОДСТВО',
    data: [
      {
        id: 1,
        name: 'валового регионального продукта',
        value: 35
      },
      {
        id: 2,
        name: 'обрабатывающей промышленности',
        value: 35
      },
      {
        id: 3,
        name: 'продукци сельского хозяйства',
        value: 28
      }
    ]
  },
  {
    id: 3,
    name: 'РЫНОК',
    data: [
      {
        id: 1,
        name: 'внейшней торговли',
        value: 54
      },
      {
        id: 2,
        name: 'розничной торговли',
        value: 35
      }
    ]
  }
]
</script>

<style lang="scss" scoped>
@import '@/assets/variables.scss';

.row {
  display: flex;
  justify-content: space-between;
  gap: 32px;

  @media #{$media} and (min-width: $mobile-min) and (max-width: $mobile-max) {
    flex-direction: column;
  }
}

.col {
  width: 33.3%;

  @media #{$media} and (min-width: $mobile-min) and (max-width: $mobile-max) {
    width: 100%;
  }

  &__title {
    font-family: $font;
    font-style: normal;
    font-weight: 700;
    font-size: 20px;
    line-height: 20px;
    color: $color-black;

    position: relative;

    &::after {
      position: absolute;
      content: '';
      width: 100%;
      height: 4px;
      background: $color-main;
      bottom: -12px;
      left: 0;
      margin: auto;
    }
  }

  &__list {
    display: flex;
    justify-content: start;
    gap: 8px;
    padding: 6px;
  }

  &__value {
    font-family: $font;
    font-style: normal;
    font-weight: 700;
    font-size: 18px;
    line-height: 24px;
    color: $color-black;
  }

  &__item {
    font-family: $font;
    font-style: normal;
    font-weight: 400;
    font-size: 18px;
    line-height: 23px;
    color: $color-grey;
  }
}

.col-wrp {
  padding: 28px 0 0 0;
}
</style>
