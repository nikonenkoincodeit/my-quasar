<template>
  <q-page class="flex flex-center">
    <div class="cart">
      <h3 class="cart-title">title</h3>
      <div class="text" v-for="item in items" :key="item" :class="'item-'+item">{{ item }}</div>
    </div>
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex',
  data: () => ({
    items: ['red', 'blue', 'green']
  })
}
</script>

<style lang="scss">
@import '../css/app';
$color: blue;
  .cart {
    width: 200px;
    height: 200px;
    background: $color;

    &:hover {
      background: $info;
    }

    .text {
      color: red;
      $items: red, blue, green;
      @each $item in $items {
        &.item-#{$item} {
          color: $item
        }
      }
    }

    &-title {
      @include colorElement(pink)
    }

  }
  
</style>