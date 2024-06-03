<template>
  <div class="table-cont">
    <h1>все кросовки</h1>
    <div>
      <select>
        <option value="option1">Option 1</option>
        <option value="option2">Option 2</option>
        <option value="option3">Option 3</option>
      </select>
      <input type="text" />
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style lang="scss" scoped>
.table-cont {
  background-color: #ffffff;
  border-radius: 10px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 2% 3%;
  box-shadow: inset -1px -1px 11px #013d00;
  h1 {
    color: #0a3300;
    font-weight: bold;
    font-size: 40px;
  }
}
</style>
