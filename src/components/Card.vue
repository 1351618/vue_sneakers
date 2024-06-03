<template>
  <div class="card">
    <button class="card__btn-cart"><img src="/like.svg" alt="" /></button>
    <button class="card__btn-add"><img src="/add.svg" alt="" /></button>
    <img :src="item.image" alt="Product Image" />
    <h4>{{ item.title }}</h4>
    <span>ЦЕНА:</span>
    <p>{{ item.price }}p</p>
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
.card {
  position: relative;
  height: 300px;
  width: 200px;
  overflow: hidden;
  border-radius: 10px;
  background-color: #fff;
  color: #013d00;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding: 13px;
  box-shadow: inset -1px -1px 11px #013d00;
  transition: box-shadow 0.1s;
  &:hover {
    box-shadow: inset -2px -2px 11px #013d00, 5px 5px 15px #012b00;
  }
  img {
    flex-grow: 1;
    object-fit: contain;
  }
  button {
    position: absolute;
    border: 2px solid #bbffb5f2;
    border-radius: 8px;
    height: 30px;
    width: 30px;
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  h4 {
    flex-grow: 1;
    font-weight: bold;
  }
  span {
    color: #013d009c;
  }
  p {
    font-weight: bold;
  }
}
.card__btn-cart {
  top: 13px;
}
.card__btn-add {
  bottom: 13px;
  right: 13px;
}
</style>
