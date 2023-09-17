<template>
  <div class="timeline">
    <TimelineTitle/>
  
      <TimelineBar class="isLargeScreen"/>
  
      <TimelineBarMobile class="isSmallScreen" />

  </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>
  .timeline{
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 24px 16px;
    margin-bottom: 72px;
    background: $color-white-background;
    .isSmallScreen{
      display: flex;
    }
    .isLargeScreen{
      display: none;
    }
    @media screen and (min-width: 1024px) {
      padding: 80px 16px;
    }
    @media screen and (min-width: 1200px) {
      .isLargeScreen{
        display: flex;
      }
      .isSmallScreen{
        display: none;
      }
    }
    
  }
</style>