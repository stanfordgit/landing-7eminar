<template>
  <div class="feedback">
    <FeedbackRegister/>
    <FeedbackStatistics/>
  </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>
  .feedback{
    display: flex;
    flex-direction: column;
    padding: 32px 16px;
    margin-bottom: 56px;
    gap: 64px;
    background: $color-white-background;
    @media screen and (min-width: 900px) {
      flex-direction: row;
      justify-content: center;
      gap: 30px;
    }
  }
</style>