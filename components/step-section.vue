<template>
  <div class="background row justify-content-start">
    <div class="container step_section_container">
      <div class="step_info col-12">3 Easy Steps to Refer</div>
      <div
        style="
          color: white;
          display: flex;
          align-items: center;
          justify-content: center;
        "
      >
        <Step
          imgPath="/_nuxt/public/assets/Step01.png"
          content="Create an account with Blackwell Global & log in to the Client Portal."
        />
        <span class="arrow">
            <Icon name="mingcute:right-fill" color="#f68b1f" />
        </span>
        <Step
          imgPath="/_nuxt/public/assets/Step02.png"
          content='Under the "Promotion" tab, copy your unique referral link & send it to your referee, or get your referee to scan your unique QR code to create an account with us.'
        />
        <span class="arrow">
            <Icon name="mingcute:right-fill" color="#f68b1f" />
        </span>
        <Step
          imgPath="/_nuxt/public/assets/Step03.png"
          content="Create an account with Blackwell Global & log in to the Client Portal."
        />
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.background {
  background-image: url(../public/assets/easy_step_bg.png);
  background-size: cover;
  background-position: center;
  height: 560px;
}

.step_section_container {
  width: 70%;
  height: 560px;
  padding: 20px;
}

.step_info {
  color: white;
  padding-bottom: 50px;
  padding-top: 25px;
  font-size: 20px;
  font-family: "";
}

.arrow {
  width: 100px;
  font-size: 50px;
  color: white;
  margin-left: 30px;
  // text-align: center;
  // font-size: 36px;
  // font-weight: bold;
}
</style>
