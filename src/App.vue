<template>
  <div
    :style="{ backgroundImage: `url(${backgroundImage})` }"
    class="background"
  >
    <Basket />
    <Header />

    <main class="bc-cont">
      <AdvertisingBanner :items="advertisingBannerData" />
      <TableCont />
      <Card :item="cardData" />
    </main>
    <Footer />
  </div>
</template>

<script setup>
import backgroundImage from "./assets/background.webp";
import Header from "./layouts/Header.vue";
import Footer from "./layouts/Footer.vue";
import AdvertisingBanner from "./components/AdvertisingBanner.vue";
import Card from "./components/Card.vue";
import TableCont from "./components/TableCont.vue";
import Basket from "./components/Basket.vue";

const advertisingBannerData = [
  {
    logo: "image 7.svg",
    img: "image 6.svg",
    backC: "#f4efe9",
    url: "/",
    text: [
      { word: " Stan Smith, ", color: "#00b13f" },
      { word: " Forever! ", color: "#000000" },
    ],
  },
  {
    logo: "image 7.svg",
    img: "image 6.svg",
    backC: "#f4efe9",
    url: "/",
    text: [
      { word: "Stan Smith,", color: "#000000" },
      { word: " Forever! -", color: "#000000" },
    ],
  },
];

const cardData = {
  image: "14317652.jpg",
  title: "Название кроссовок",
  description: "Описание кроссовок",
  price: 1234,
};
</script>

<style lang="scss" scoped>
.background {
  background-size: cover;
  background-position: center;
  width: 100%;
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
}

.bc-cont {
  background: linear-gradient(135deg, #ffffff42, #ffffff2b);
  backdrop-filter: blur(10px);
  max-width: 1400px;
  width: 100%;
  border-radius: 20px;
  border: 1px solid #ffffff2b;
  box-shadow: 0px 8px 32px #00000094;
  margin: 10px 0 0 0;
  color: #e7ffe7;
  padding: 1%;
}

main {
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  gap: 1%;
}

footer {
  min-height: 70px;
}
</style>
