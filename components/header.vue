<template>
  <div class="row justify-content-start d-flex header-background">
    <div class="col-4 justify-content-center align-items-center d-flex">
      <img class="logo-header" src="../public/assets/logo-white.png" />
    </div>
    <div class="col-1" style="display: flex">
      <div
        class="pt-3 d-flex justify-content-center align-items-start"
        style="width: 75px"
      >
        <div class="promotion-text">PROMOTION END IN</div>
      </div>
    </div>
    <div class="col-5 d-flex justify-content-start countdown-timer">
      <div class="timer-item row">
        <span class="timer-value">{{ countdown.days }}</span>
        <span class="timer-label">Days</span>
      </div>
      <span class="timer-value pb-4">:</span>
      <div class="timer-item row">
        <span class="timer-value">{{ countdown.hours }}</span>
        <span class="timer-label">Hours</span>
      </div>
      <span class="timer-value pb-4">:</span>
      <div class="timer-item row">
        <span class="timer-value">{{ countdown.minutes }}</span>
        <span class="timer-label">Minutes</span>
      </div>
      <span class="timer-value pb-4">:</span>
      <div class="timer-item row">
        <span class="timer-value">{{ countdown.seconds }}</span>
        <span class="timer-label">Seconds</span>
      </div>
    </div>
    <div class="col-2 pt-2 col d-flex">
      <div
        class="justify-content-center align-items-center d-flex register-button"
      >
        <div class="register-text">REGISTER NOW</div>
      </div>
      <div
        @click="openDropDownAction"
        style="cursor: pointer"
        class="justify-content-center align-items-center d-flex ms-3 pb-2 w-10"
      >
        <Icon style="color: #818181" name="iconamoon:profile-fill" />
      </div>
      <div
        v-if="openDropDown"
        class="justify-content-center align-items-center"
        style="
          width: 50px;
          height: 40px;
          background-color: #282d39;
          position: absolute;
          top: 40px;
          right: 100px;
          color: #fff;
        "
      >
        Login
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref, computed, onMounted } from 'vue';

const promotionEndDate = new Date('2024-05-01T00:00:00'); // Set your promotion end date here
const currentTime = ref(new Date());

const countdown = computed(() => {
  const timeDifference = promotionEndDate.getTime() - currentTime.value.getTime();
  if (timeDifference <= 0) {
    return { days: 0, hours: 0, minutes: 0, seconds: 0 };
  }
  const seconds = Math.floor(timeDifference / 1000);
  const minutes = Math.floor(seconds / 60);
  const hours = Math.floor(minutes / 60);
  const days = Math.floor(hours / 24);

  return {
    days: days,
    hours: hours % 24,
    minutes: minutes % 60,
    seconds: seconds % 60
  };
});

// Update current time every second
onMounted(() => {
  setInterval(() => {
    currentTime.value = new Date();
  }, 1000);
});

const openDropDown = ref(false);

function openDropDownAction() {
  openDropDown.value = true;
}

</script>

<style lang="scss">
.header-background {
  background-color: #102a4c;
}

.register-button {
  background-image: linear-gradient(to top, #eb6b23, #f68a1e);
  width: 100px;
  height: 30px;
  border-radius: 15px;
  margin-top: 5px;
}

.register-text {
  font-size: 10px;
  font-weight: 700;
  color: #fce6d9;
}

.logo-header {
  width: 80px;
  height: 20px;
}

.promotion-text {
  color: #b9e6f9;
  font-size: 10px;
  text-align: center;
}

.countdown-timer {
  display: flex;
  justify-content: center;
  align-items: center;
}

.timer-item {
  margin: 0 10px;
  text-align: center;
}

.timer-item .row {
  padding-left: 0 !important;
  padding-right: 0 !important;
}

.timer-value {
  font-size: 24px;
  font-weight: 500;
  color: #f0f2f4;
}

.timer-label {
  font-size: 14px;
  color: #f0f2f4;
}
</style>
