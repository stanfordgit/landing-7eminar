<template>
  <div class="tariff__info">
    <div class="title-row">
      Оплачуйте пакети <span class="focus">частинами без комісії</span>!
    </div>
    <div class="title-row">
      Натискайте на кнопку <span class="focus">Оплатити карткою</span> та оформлюйте розстрочку
    </div>
    <div class="title-row">через PrivatBank або Monobank</div>
  </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>
.tariff__info{
  margin-top: 24px;
  text-align: center;
  font-family: 'Raleway', sans-serif;
  font-size: 17px;
  font-weight: 500;
  line-height: 150%;
  text-wrap: balance;

  .focus{
    font-weight: 700;
  }
  @media screen and (min-width: 500px) {
     font-size: 17px;
     display: inline;
  }
 }
</style>