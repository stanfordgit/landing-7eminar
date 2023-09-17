<template>
  <div class="tariff">
    <TariffTop/>
    <TariffTimer class="isSmallScreen"/>
    <TariffPlans class="isLargeScreen"/>
    <TariffPlansMobile class="isSmallScreen"/>
    <TariffInfo/>
  </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>
  .tariff{
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 0 16px;
    margin-bottom: 72px;
    .isSmallScreen{
        display: flex;
    }
    .isLargeScreen{
      display: none;
    }
    @media screen and (min-width: 1100px) {
      .isLargeScreen{
        display: flex;
      }
      .isSmallScreen{
        display: none;
      }
    }
  }
</style>