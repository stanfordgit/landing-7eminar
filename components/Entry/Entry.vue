<template>
  <div class="entry">
    <EntryTop/>
    <EntrySlider class="isSmallScreen"/>
    <EntryPhoto class="isLargeScreen"/>
    <EntryOffer/>
  </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>
  .entry{
    display: flex;
    flex-direction: column;
    margin: 40px 0 72px;
    padding: 0 0px 24px;
    background: $color-white-background;
    .isLargeScreen{
      display: none;
    }
    @media screen and (min-width: 960px) {
      margin: 64px 0 104px;
      padding-bottom: 48px;

    }
    @media screen and (min-width: 960px) {
      .isLargeScreen{
        align-self: center;
        display: flex;
      }
      .isSmallScreen{
        display: none;
      }
    }
  }
</style>