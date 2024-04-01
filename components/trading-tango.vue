<template>
  <div class="background-header">
    <div class="container pt-5 pb-5">
      <div class="row g-2">
        <div class="col-5 justify-content-center d-flex ps-5">
          <img style="width: 150px" src="../public/assets/logomark.png" />
        </div>
        <div class="col-7">
          <div class="row pe-5">
            <div
              class="justify-content-center d-flex align-items-center trading-tango"
            >
              TRADING TANGO
            </div>
            <div
              class="justify-content-center d-flex align-items-center valentine"
            >
              VALENTINE'S DAY PROMOTION
            </div>
            <div class="justify-content-center d-flex align-items-center date">
              1 - 29 February 2024
            </div>
            <div>
              <div
                class="justify-content-center d-flex align-items-center termCondition"
              >
                <a href="#" style="color: #f68b1f">Term & conditions</a>&nbsp;apply
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <CollectReward />
  </div>
</template>

<style lang="scss">
.background-header {
  background-image: url(../public/assets/Trading-Tango-header.png);
  background-size: cover;
  background-position: center;
  height: 560px;
}

.trading-tango {
  font-size: 45px;
  font-weight: 600;
  color: #b9e6f9;
}

.date {
  font-size: 20px;
  font-weight: 400;
  color: #b9e6f9;
}

.termCondition {
  font-size: 10px;
  font-weight: 400;
  color: #b9e6f9;
}

.valentine {
  font-size: 25px;
  font-weight: 500;
  color: #b9e6f9;
}
</style>
