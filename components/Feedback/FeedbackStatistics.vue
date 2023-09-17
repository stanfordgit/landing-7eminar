<template>
  <div class="feedback__statistics statistics">
    <div class="statistics__title">З передплатою Академії ви отримаєте:</div>
    <div class="statistics__block block">
      <div class="block__item item">
        <div class="item__title">8+</div>
        <div class="item__description">Професійних курсів</div>
      </div>
      <div class="block__item item">
        <div class="item__title">12</div>
        <div class="item__description">Закритих клубних лекцій</div>
      </div>
      <div class="block__item item">
        <div class="item__title">48</div>
        <div class="item__description">Нових вебінарів та тренінгів</div>
      </div>
      <div class="block__item item">
        <div class="item__title">
          <svg xmlns="http://www.w3.org/2000/svg" height="58" width="58" viewBox="0 0 58 58" fill="none">
            <path d="M13.619 38.6663C7.0312 38.6663 4.83203 33.833 4.83203 28.9997C4.83203 24.1663 7.0312 19.333 13.619 19.333C22.4084 19.333 35.5889 38.6663 44.3784 38.6663C50.9662 38.6663 53.1654 33.833 53.1654 28.9997C53.1654 24.1663 50.9662 19.333 44.3784 19.333C35.5889 19.333 22.4084 38.6663 13.619 38.6663V38.6663Z" stroke="#0066CC" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </div>
        <div class="item__description">Безлімітні відповіді на запитання протягом навчання</div>
      </div>
    </div>
    <div class="statistics__tasks">
      <div class="tasks__title">Тестові та практичні</div>
      <div class="tasks__description">завдання зі зворотним зв'язком</div>
    </div>
  </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>
  .feedback__statistics{
    @media screen and (min-width: 500px) {
      padding: 0 32px;
    }
    .statistics__title{
      font-family: "eUkraineHead", sans-serif;
      font-size: 24px;
      font-weight: 600;
      line-height: 140%;
      @media screen and (min-width: 500px) {
        font-size: 23px;
        width: 450px;
      }
    }
    .statistics__block{
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      grid-column-gap:15px;
      grid-row-gap: 15px;
      margin-top: 24px;

      @media screen and (min-width: 500px) {
        grid-template-columns: repeat(2, 190px);
        grid-column-gap:0px;
        grid-row-gap: 0px;
        margin-bottom: 0px;
      }
      .block__item {
        display: flex;
        flex-direction: column;
        .item__title{
          display: flex;
          height: 58px;
          font-family: "eUkraineHead", sans-serif;
          font-size: 43px;
          font-weight: 300;
          line-height: 150%;
          color: $color-blue-primary;
          @media screen and (min-width: 500px) {
            font-size: 63px;
            height: 88px;
            svg{
              height: 88px;
              width: 88px;
            }
          }
        }
        .item__description{
          display: flex;
          align-items: flex-start;
          font-family: "Raleway", sans-serif;
          font-size: 16px;
          font-weight: 400;
          line-height: 150%;
          @media screen and (min-width: 500px) {
            font-size: 17px;
          }
        }
      }
    }
    .statistics__tasks{
      display: flex;
      flex-direction: column;
      
      margin-top: auto;
      .tasks__title{  
        font-family: "Raleway", sans-serif;
        font-size: 24px;
        font-weight: 700;
        line-height: 150%;
        color: $color-blue-primary;
        @media screen and (min-width: 500px) {
          font-size: 39px;
        }
      }
      .tasks__description{
        font-family: "Raleway", sans-serif;
        font-size: 16px;
        font-weight: 400;
        line-height: 150%;
        @media screen and (min-width: 500px) {
          font-size: 17px;
        }
      }
    }
  }
</style>