<template>
  <div class="selected-product-card">
    <img :src="item.image" alt="Product Image" />
    <div class="selected-product-card__cont">
      <h4>{{ item.title }}</h4>

      <p>
        ЦЕНА:<br />
        {{ item.price }}p
      </p>
    </div>
    <button>X</button>
  </div>
</template>
<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps<{
  item: {
    image: string;
    title: string;
    description: string;
    price: number;
  };
}>();
</script>
<style lang="scss" scoped>
.selected-product-card {
  position: relative;
  display: flex;
  flex-direction: row;
  height: 120px;
  width: 100%;
  gap: 10px;
  border: 2px solid #013d00;
  border-radius: 10px;
  overflow: hidden;
  padding: 2%;

  button {
    position: absolute;
    right: 10px;
    bottom: 10px;
    height: 30px;
    width: 30px;
    border: none;
    background-color: #ff00004a;
    border-radius: 5px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
}

.selected-product-card__cont {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
</style>
