<template>
  <div class="tariff__timer timer">
    <div class="timer__data">
      <div class="data__hours">{{ hours }}<div class="type-data">год</div></div>
      <span>:</span>
      <div class="data__minutes">{{ minutes }}<div class="type-data">хв</div></div>
      <span>:</span>
      <div class="data__seconds">{{ seconds }}<div class="type-data">сек</div></div>
    </div>
  </div>
</template>

<script setup>
      const targetTime = new Date('Oct 3, 2023 17:00:00').getTime();
      const currentTime = ref(null);
      const reamingTime = ref(null);
      let timerInterval;
      const hours = computed(() => {
        const reamingHours = Math.floor(reamingTime.value / (1000 * 60 * 60));
        return String(reamingHours).padStart(2, '0');
      })
      const minutes = computed(() => {
        const reamingMinutes = Math.floor((reamingTime.value / 1000 / 60) % 60);
        return String(reamingMinutes).padStart(2, '0');
      })
      const seconds = computed(() => {
        const reamingSeconds = Math.floor((reamingTime.value / 1000) % 60);
        return String(reamingSeconds).padStart(2, '0');
      })
      const updateCurrentTime = () => {
        currentTime.value = new Date().getTime();
        const timeLeft = targetTime - currentTime.value;
        reamingTime.value = timeLeft > 0 ? timeLeft : 0
      };
      onMounted(() => {
        timerInterval = setInterval(updateCurrentTime, 1000);
      });
      onUnmounted(()=>{
        clearInterval(timerInterval);
      })
</script>

<style lang="scss" scoped>
  .tariff__timer{
    display: flex;
    flex-direction: column;
    margin-top: 16px;
    margin-bottom: 24px;
    gap: 16px;

    .timer__data{
      display: flex;
      position: relative;
      justify-content: center;
      gap: 6px;

      font-family: "Raleway", sans-serif;
      font-size: 30px;
      font-weight: 400;
      line-height: 150%;
      color: $color-blue-primary;
      .type-data{
        text-align: center;
        font-family: "Raleway", sans-serif;
        font-size: 16px;
        font-weight: 400;
        line-height: 80%;
      }
      .data__hours,
      .data__minutes{
        opacity: 0.4;
      }
    }
  }
</style>