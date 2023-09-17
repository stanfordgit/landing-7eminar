<template>
  <div class="entry__slider slider">
    <swiper
    class="swiper-container"
    :modules="modules"
    :slides-per-view="2"
    :initial-slide="1"
    :space-between="30"
   
    centered-slides
    :navigation="{
      prevEl: '.swiper-button-prev',
      nextEl: '.swiper-button-next',
    }"
  >
    <swiper-slide>
      <div class="block__item">
        <img src="/images/slider/slider_1.png" alt="photo_1">
        <div class="text">Професії: <span class="focus-bold">Головбух, Фіндир, HR</span></div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="block__item">
        <img src="/images/slider/slider_2.png" alt="photo_2">
        <div class="text"><span class="focus-bold">Закриті клубні лекції</span></div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="block__item">
        <img src="/images/slider/slider_3.png" alt="photo_3">
        <div class="text">Підвищення кваліфікації: <span class="focus-bold">ПДВ, ЗП, ЗЕД, ФОП та ін.</span></div>
      </div>
    </swiper-slide>
    
  </swiper>
  <div class="slider__buttons">
      <div ref="prev" class="swiper-button-prev"><svg xmlns="http://www.w3.org/2000/svg" width="45" height="44" viewBox="0 0 45 44" fill="#232323">
    <path d="M22.5356 37.021C30.7356 37.021 37.5356 30.221 37.5356 22.021C37.5356 13.821 30.7356 7.021 22.5356 7.021C14.3356 7.021 7.53564 13.821 7.53564 22.021C7.53564 30.221 14.3356 37.021 22.5356 37.021ZM22.5356 35.021C15.2356 35.021 9.43565 29.221 9.43565 22.021C9.43565 14.821 15.2356 8.92099 22.4356 8.92099C29.6356 8.92099 35.5356 14.721 35.5356 22.021C35.5356 29.221 29.7356 35.021 22.5356 35.021ZM25.3356 29.321C25.6356 29.021 25.6356 28.421 25.3356 28.121L18.9356 22.021L25.3356 15.921C25.7356 15.621 25.6356 15.021 25.3356 14.721C25.0356 14.421 24.4356 14.421 24.1356 14.721L17.6356 20.921C16.9356 21.521 16.9356 22.521 17.6356 23.121L24.1356 29.321C24.4356 29.621 25.0356 29.721 25.3356 29.321Z"/>
    </svg></div>
        <div ref="next" class="swiper-button-next"><svg xmlns="http://www.w3.org/2000/svg" width="45" height="44" viewBox="0 0 45 44" fill="#232323">
    <path d="M22.5356 37.021C30.7356 37.021 37.5356 30.221 37.5356 22.021C37.5356 13.821 30.7356 7.021 22.5356 7.021C14.3356 7.021 7.53564 13.821 7.53564 22.021C7.53564 30.221 14.3356 37.021 22.5356 37.021ZM22.5356 35.021C15.2356 35.021 9.43565 29.221 9.43565 22.021C9.43565 14.821 15.2356 8.92099 22.4356 8.92099C29.6356 8.92099 35.5356 14.721 35.5356 22.021C35.5356 29.221 29.7356 35.021 22.5356 35.021ZM19.2356 29.321C19.5356 29.621 20.1356 29.621 20.5356 29.321L27.0356 23.121C27.7356 22.521 27.7356 21.521 27.0356 20.921L20.5356 14.721C20.1356 14.321 19.6356 14.321 19.3356 14.721C18.9356 15.021 18.9356 15.621 19.3356 15.921L25.7356 22.021L19.3356 28.121C18.8356 28.421 18.8356 29.021 19.2356 29.321Z"/>
    </svg></div>
</div>
 
  </div>
</template>

<script setup>
  import { Swiper, SwiperSlide } from 'swiper/vue';
  import { Navigation } from 'swiper/modules';

import 'swiper/css';
import 'swiper/css/navigation';

const modules = [Navigation]

</script>

<style lang="scss" scoped>
.entry__slider{
  margin: 40px 0;
  .swiper {
      display: flex;
      height: 640px;
  }
  .swiper-slide {
    display: flex;
    justify-content:center;
    align-self: flex-end;
    height: 590px;
    transition: margin-bottom 0.5s ease;

      &.swiper-slide-active{
        margin-bottom: 48px;
        z-index: 1;
      }
      .block__item{
      position: relative;
      display: flex;
      justify-content: center;
      text-align: center;
 
      img{
        max-width: 290px;
        height: auto;
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
  .slider__buttons{
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .swiper-button-prev,
  .swiper-button-next {
    &.swiper-button-disabled{
      svg{
          fill: #86868B;
      }
   
    }
    all: unset;
    width: 44px;
    height: 44px;
    cursor: pointer;
  }

  
  
}
</style>