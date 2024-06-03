<template>
  <div class="basket">
    <h1>Корзина</h1>
    <div class="selected-products">
      <SelectedProductCard :item="cardData" />
    </div>
    <p>сумма</p>
  </div>
</template>
<script setup lang="ts">
import SelectedProductCard from "./SelectedProductCard.vue";

const cardData = {
  image: "14317652.jpg",
  title: "Название кроссовок",
  description: "Описание кроссовок",
  price: 1234,
};
</script>
<style lang="scss" scoped>
.basket {
  position: absolute;
  background-color: white;
  z-index: 100;
  right: 0;
  height: 100%;
  width: 30%;
  box-shadow: inset -1px -1px 11px #013d00;
  border-radius: 10px;
  padding: 2%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.selected-products {
  flex-grow: 1;
  display: flex;
  flex-direction: column;
}
</style>
