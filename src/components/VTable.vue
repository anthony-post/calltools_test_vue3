<template>
  <aside class="table table-wrp">
    <table>
      <tr>
        <th class="table__title">Рост за 2019 год</th>
        <th class="table__header-colored">Центральная Россия</th>
        <th class="table__header">Российская Федерация</th>
      </tr>
      <tr v-for="item in dataIndicators" :key="item.id">
        <td class="table__name">
          <v-icon :icon-id="item?.icon" width="40" height="40" />{{ item.name }}
        </td>
        <td class="table__value-colored">{{ item.rfCenter }}</td>
        <td class="table__value">{{ item.rf }}</td>
      </tr>
    </table>
  </aside>
</template>

<script setup>
import VIcon from '@/components/VIcon.vue'

const dataIndicators = [
  {
    id: 1,
    name: 'Внешняя торговля',
    rfCenter: '+19.0 %',
    rf: '+17.6 %',
    icon: 'icon-trade'
  },
  {
    id: 2,
    name: 'Инвестиции',
    rfCenter: '+8.9 %',
    rf: '+4.3 %',
    icon: 'icon-currency'
  },
  {
    id: 3,
    name: 'Промышленность',
    rfCenter: '+7.5 %',
    rf: '+2.9 %',
    icon: 'icon-gear'
  },
  {
    id: 4,
    name: 'Розничная торговля',
    rfCenter: '+4.0 %',
    rf: '+2.6 %',
    icon: 'icon-cart'
  },
  {
    id: 5,
    name: 'Сельское хозяйство',
    rfCenter: '+3.1 %',
    rf: '-0.6 %',
    icon: 'icon-agriculture'
  }
]
</script>

<style lang="scss" scoped>
@import '@/assets/variables.scss';
.table {
  background-color: $color-table;

  &__title {
    font-family: $font;
    font-style: normal;
    font-weight: 700;
    font-size: 18px;
    line-height: 24px;
    text-align: left;
    color: $color-main;
    
    width: 50%;
  }

  &__header {
    font-family: $font;
    font-style: normal;
    font-weight: 500;
    font-size: 12px;
    line-height: 15px;
    text-align: right;
    color: $color-grey;
  }

  &__header-colored {
    font-family: $font;
    font-style: normal;
    font-weight: 500;
    font-size: 12px;
    line-height: 15px;
    text-align: center;
    color: $color-main;
  }

  &__name {
    font-family: $font;
    font-style: normal;
    font-weight: 400;
    font-size: 18px;
    line-height: 23px;
    color: $color-black;

    display: flex;
    align-items: center;
  }

  &__value {
    font-family: $font;
    font-style: normal;
    font-weight: 700;
    font-size: 20px;
    line-height: 20px;
    text-align: right;
    color: $color-grey;
  }

  &__value-colored {
    font-family: $font;
    font-style: normal;
    font-weight: 700;
    font-size: 20px;
    line-height: 20px;
    text-align: right;
    color: $color-main;
  }
}

.table-wrp {
  width: 546px;
  padding: 20px 18px 20px 34px;
  margin-top: 47px;
}
</style>
