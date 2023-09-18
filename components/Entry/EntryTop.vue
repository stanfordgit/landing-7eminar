<template>
  <div class="entry__top top">
    <div class="top__name">Вища Бухгалтерська Online-Академія</div>
    <h3 class="top__title">Підвищення кваліфікації та профперепідготовка для бухгалтерів</h3>
    <v-button buttonClass="default">Обрати навчання >></v-button>
  </div>
</template>

<script setup>
</script>

<style lang="scss" scoped>
  .entry__top{
    padding: 0 24px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: 0 16px;
    .top__name{
      font-family: "Raleway", sans-serif;
      font-size: 18px;
      font-weight: 500;
      line-height: 25px;
      @media screen and (min-width: 500px) {
        font-size: 17px;
      }
    }
    .top__title{
      margin: 21px 0;
      font-family: "eUkraineHead", sans-serif;
      font-size: 24px;
      font-weight: 600;
      line-height: 150%;
      text-wrap: balance;
      @media screen and (min-width: 500px) {
        margin: 22px 0;
        font-size: 42px;
      }
    }
  }
</style>