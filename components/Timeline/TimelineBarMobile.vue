<template>
  <div class="timeline__bar-mobile">
    <div class="progress-container">
      <div id="mobile-mark-start" class="scale-mark" data-date="2023-08-10"></div>
      <div id="mobile-mark-aug21" class="scale-mark" data-date="2023-08-21">21 серпня</div>
      <div id="mobile-mark-sep1" class="scale-mark" data-date="2023-09-01">1 вересня</div>
      <div id="mobile-mark-sep15" class="scale-mark" data-date="2023-09-15">15 вересня</div>
      <div id="mobile-mark-oct3" class="scale-mark" data-date="2023-10-03">3 жовтня</div>
      <div id="mobile-progress-bar" class="progress-bar"> 
        <div class="moving-circle"></div>
      </div>
      <div class="increase">
        <div class="increase__item increase-start">Ціни раннього<br>бронювання</div>
        <div class="increase__item increase-10">Подорожчання<br>на 10%</div>
        <div class="increase__item increase-15">Подорожчання<br>на 15%</div>
        <div class="increase__item increase-end">Можливо квитки<br>вже закінчаться</div>
      </div>
    </div>

  </div>
</template>

<script setup>
onMounted(()=>{
  updateCirclePositionMobile()
})
function updateCirclePositionMobile() {

    const currentDate = new Date();
    
    const progressBar = document.getElementById('mobile-progress-bar');
    const markStart = document.getElementById('mobile-mark-start'); 
    const markAug21 = document.getElementById('mobile-mark-aug21');  
    const markSep1 = document.getElementById('mobile-mark-sep1');  
    const markSep15 = document.getElementById('mobile-mark-sep15');  
    const markOct3 = document.getElementById('mobile-mark-oct3');

  
    const startDate = new Date(markStart.dataset.date);
    const endDate = new Date(markOct3.dataset.date);

    markStart.style.top = '0%';
    markAug21.style.top = `${((new Date(markAug21.dataset.date) - startDate)/(endDate - startDate)) * 100}%`;
    markSep1.style.top = `${((new Date(markSep1.dataset.date) - startDate)/(endDate - startDate)) * 100}%`;
    markSep15.style.top = `${((new Date(markSep15.dataset.date) - startDate)/(endDate - startDate)) * 100}%`;
    markOct3.style.top = '100%';

    const progress = ((currentDate - startDate) / (endDate - startDate)) * 100;
    progressBar.style.height = `${progress}%`;
}
</script>

<style lang="scss" scoped>
  .timeline__bar-mobile{
    display: flex;
    justify-content: center;
    position: relative;
    margin-top: 40px;
    margin-bottom: 20px;  
    .progress-container{
      display: flex;
      width: 6px;
      height: 678px;
      background-color: #F6F6F6;
      line-height: 0;
      position: relative;
      .progress-bar{
        width: 6px;
        max-height: 100%;
        position: absolute;
        top: 0;

        left: 0;
        background: $color-black-content;
      }
      .scale-mark{
        position: absolute;
        display: flex;
        white-space: nowrap;
        font-family: 'Raleway', sans-serif;
        font-size: 16px;
        right: 30px;
        font-weight: 700;
        &::after{
          content: '';
          position: absolute;
          width: 17px;
          height: 3px;
          top: -1px;
          right: -35.5px;
          background: $color-black-content;
        }
      }

      .moving-circle{
        width: 33px;
        height: 33px;
        background: #FFE601;
        border: 3px solid $color-black-content;
        box-sizing:border-box;
        border-radius: 50%;
        position: absolute;
        bottom: -16.5px;
        left: -13.5px;
        &::after{
          content: '';
          width: 13px;
          height: 13px;
          position: absolute;
          top: 0;
          left: 0;
          right: 0;
          bottom: 0;
          margin: auto;
          border-radius: 50%;
          background: $color-black-content;
        }
      }
    }
    .increase{
      position: absolute;
      white-space: nowrap;
      font-family: 'Raleway',sans-serif;
      height: 100%;
      left: 30px;
      font-size: 16px;
      font-weight: 400;
      line-height: 130%;
      .increase__item{
        position: absolute;

      }
      .increase-start{
        top: -6px;
      }
      .increase-10{
        top: 27%;
      }
      .increase-15{
        top: 51% ;
      }
      .increase-end{
        bottom: -10px;
      }
    }
  }
</style>