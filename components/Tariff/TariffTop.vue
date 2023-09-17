<template>
  <div class="tariff__top top">
    <h3 class="top__title"><div class="title-row"><span class="upper">Передплата на</span> Вищу Бухгалтерську</div> Онлайн-Академію</h3>
    <div class="top__timer-title">Оберіть свій тарифний пакет:</div>
  </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>
  .tariff__top{
    display: flex;
    flex-direction: column;
    gap: 16px;
    font-family: "eUkraineHead", sans-serif;
    font-size: 24px;
    font-weight: 600;
    line-height: 140%;
    text-align: center;
    text-wrap: balance;
    @media screen and (min-width: 500px) {
      font-size: 42px;
      .top__title {   
        display: inline;
      }
    }
    @media screen and (max-width: 500px) {
      .upper{
        text-transform: uppercase;
      }
    }
    .top__timer-title{
      font-family: "Raleway", sans-serif;
      font-size: 18px;
      font-weight: 700;
      line-height: 28px;
    }
  } 
</style>