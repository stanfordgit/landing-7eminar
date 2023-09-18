<template>
  <div class="entry__photo photo">
    <div class="photo__block block">
      <div class="block__item">
        <img src="/images/slider/slider_1.png" alt="photo_1">
        <div class="text">Професії: <span class="focus-bold">Головбух, Фіндир, HR</span></div>
      </div>
      <div class="block__item">
        <img src="/images/slider/slider_2.png" alt="photo_2">
        <div class="text"><span class="focus-bold">Закриті клубні лекції</span></div>
      </div>
      <div class="block__item">
        <img src="/images/slider/slider_3.png" alt="photo_3">
        <div class="text">Підвищення кваліфікації: <span class="focus-bold">ПДВ, ЗП, ЗЕД, ФОП та ін.</span></div>
      </div>
    </div>
  </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>
.entry__photo{
  margin: 40px 0;
  .photo__block{
    display: flex;
    justify-content: center;
    align-items: flex-end;
    gap: 26px;
    height: 640px;
    .block__item{
      position: relative;
      display: flex;
      justify-content: center;
      text-align: center;
      height: 590px;
      &:nth-child(2)
      {
        margin-bottom: 48px;
      }
      img{
        height: 100%;
      }
      .text{
        width: 240px;
        height: 179px;
        position: absolute;
        display: flex;
        flex-direction: column;
        justify-content: center;
        border-radius: 10px;
        bottom:140px;
        backdrop-filter: blur(40px);

        font-family: 'eUkraineHead', sans-serif;
        font-size: 26px;
        font-weight: 100;
        line-height: 150%;
        color: $color-white-background;
        .focus-bold{
          font-weight: 600;
        }
        &:nth-child(1){
        
          background: linear-gradient(0deg, rgba(255, 255, 255, 0.12) 0%, rgba(255, 255, 255, 0.12) 100%), rgba(255, 255, 255, 0.11);
        }
        &:nth-child(2){
          background: rgba(255, 255, 255, 0.25);
        }
        &:nth-child(3){
          background: linear-gradient(0deg, rgba(35, 35, 35, 0.18) 0%, rgba(35, 35, 35, 0.18) 100%), rgba(255, 255, 255, 0.11);
        backdrop-filter: blur(40px);
        }
      }
    }
  }
}
</style>