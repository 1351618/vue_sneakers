<template>
  <div
    class="advertising-banner"
    :style="{ backgroundColor: items[bannerDispId].backC }"
  >
    <img
      class="advertising-banner__logo"
      :src="items[bannerDispId].logo"
      alt="advertising logo img"
    />
    <p>
      <span
        v-for="(item, index) in items[bannerDispId].text"
        :key="index"
        :style="{ color: item.color }"
      >
        {{ item.word }}
      </span>
    </p>
    <img
      class="advertising-banner__img"
      :src="items[bannerDispId].img"
      alt="advertising banner img"
    />
  </div>
</template>

<script setup lang="ts">
import { defineProps } from "vue";

const bannerDispId = 0;

const props = defineProps<{
  items: Array<{
    img: string;
    logo: string;
    backC: string;
    url: string;
    text: Array<{ word: string; color: string }>;
  }>;
}>();
</script>

<style lang="scss" scoped>
.advertising-banner {
  display: flex;
  flex-direction: row;
  position: relative;
  justify-content: space-between;
  border-radius: 20px;
  align-items: center;
  height: 300px;
  //   box-shadow: inset -1px -1px 11px #013d00;
  overflow: hidden;

  p {
    font-size: 43px;
    font-weight: bold;
    padding-left: 6%;
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    align-items: center;
    z-index: 1;
  }
}
.advertising-banner__logo {
  position: absolute;
  top: 10px;
  left: 10px;
  z-index: 1;
}
.advertising-banner__img {
  position: absolute;
  right: 0;
}
</style>
