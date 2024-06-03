<template>
  <header class="bc-cont">
    <div class="logo">
      <img src="/logo.jpg" alt="Logo" />
      <div class="logo__text">
        <p>VUE SNEAKERS</p>
        <span> Магазин лучших кроссовок </span>
      </div>
    </div>
    <div class="nav">
      <div class="cart nav__ocnt">
        <img src="/cart.svg" alt="" />
        <p>1234p</p>
      </div>
      <div class="bookmarks nav__ocnt">
        <img src="/bookmarks.svg" alt="" />
        <p>Закладки</p>
      </div>
      <div class="profile nav__ocnt">
        <img src="/profile.svg" alt="" />
        <p>Профиль</p>
      </div>
    </div>
  </header>
</template>

<script setup></script>

<style lang="scss" scoped>
header {
  min-height: 70px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.logo {
  display: flex;
  align-items: center;
  gap: 8px;
  img {
    height: 33px;
    border-radius: 50% 20%;
  }
}
.logo__text {
  p {
    font-size: 20px;
    font-weight: 600;
  }
  span {
    font-size: 13px;
  }
}
.nav {
  display: flex;
  gap: 20px;
}
.nav__ocnt {
  display: flex;
  gap: 10px;
}
</style>
