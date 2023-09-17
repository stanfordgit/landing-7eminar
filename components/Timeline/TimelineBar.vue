<template>
  <div class="timeline__bar">
    <div class="progress-container">
      <div id="mark-start" class="scale-mark" data-date="2023-08-10"></div>
      <div id="mark-aug21" class="scale-mark" data-date="2023-08-21"><div class="date">21 серпня</div></div>
      <div id="mark-sep1" class="scale-mark" data-date="2023-09-01"><div class="date">1 вересня</div></div>
      <div id="mark-sep15" class="scale-mark" data-date="2023-09-15"><div class="date">15 вересня</div></div>
      <div id="mark-oct3" class="scale-mark" data-date="2023-10-03"><div class="date">3 жовтня</div></div>
      <div id="progress-bar" class="progress-bar"> 
        <div class="moving-circle"></div>
      </div>
      <div class="increase">
        <div class="increase__item increase-start">Ціни раннього<br>бронювання</div>
        <div class="increase__item increase-10">Подорожчання<br>на 10%</div>
        <div class="increase__item increase-15">Подорожчання<br>на 15%</div>
        <div class="increase__item increase-end">Квитки<br>вже закінчаться</div>
      </div>
    </div>

  </div>
</template>

<script setup>
onMounted(()=>{
  updateCirclePosition()
})
function updateCirclePosition() {

    const currentDate = new Date();
    
    const progressBar = document.getElementById('progress-bar');
    const markStart = document.getElementById('mark-start'); 
    const markAug21 = document.getElementById('mark-aug21');  
    const markSep1 = document.getElementById('mark-sep1');  
    const markSep15 = document.getElementById('mark-sep15');  
    const markOct3 = document.getElementById('mark-oct3');

  
    const startDate = new Date(markStart.dataset.date);
    const endDate = new Date(markOct3.dataset.date);

    markStart.style.left = '0%';
    markAug21.style.left = `${((new Date(markAug21.dataset.date) - startDate)/(endDate - startDate)) * 100}%`;
    markSep1.style.left = `${((new Date(markSep1.dataset.date) - startDate)/(endDate - startDate)) * 100}%`;
    markSep15.style.left = `${((new Date(markSep15.dataset.date) - startDate)/(endDate - startDate)) * 100}%`;
    markOct3.style.left = '100%';

    const progress = ((currentDate - startDate) / (endDate - startDate)) * 100;
    progressBar.style.width = `${progress}%`;
}
</script>

<style lang="scss" scoped>
  .timeline__bar{
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    margin-top: 40px;
    height: 158px;
    .progress-container{
      display: flex;
      height: 6px;
      width: 1090px;
      background-color: #F6F6F6;
      line-height: 0;
      position: relative;
      .progress-bar{
        height: 6px;
        max-width: 100%;
        position: absolute;
        top: 0;
        left: 0;
        background: $color-black-content;
      }
      .scale-mark{
        position: relative;
        font-family: 'Raleway', sans-serif;
        font-size: 16px;
        top: 50px;
        font-weight: 700;
        .date{
          position: absolute;
          display: flex;
          white-space: nowrap;
          align-items: center;
          left: -40px;
        }
        &::after{
          content: '';
          position: absolute;
          width: 3px;
          height: 17px;
          bottom: 44.5px;
          left: -1.5px;
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
        bottom: -13.5px;
        right: -13.5px;
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
      display: flex;
      align-items: center;
      white-space: nowrap;
      font-family: 'Raleway',sans-serif;
      width: 100%;
      bottom: 70px;
      font-size: 16px;
      font-weight: 400;
      line-height: 130%;
      .increase__item{
        position: absolute;
      }
      .increase-start{
        left: 0;
        text-align: left;
      }
      .increase-10{
        left: 26%;
        text-align: center;
      }
      .increase-15{
       left: 49% ;
       text-align: center;
      }
      .increase-end{
        text-align: right;
        right: 0;
      }
    }
  }
</style>