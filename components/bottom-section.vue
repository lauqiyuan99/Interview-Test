<template>
  <div class="bottom-container">
    <div class="content-container">
      <span style="margin: 30px" class="bottom_span_info"
        >LOG IN TO MT4 DESKTOP APP</span
      >

      <button class="btn download_platform_button">Download Platform</button>

      <span style="margin: 30px" class="bottom_span_info"
        >LOG IN VIA MT4 MOBILE APP</span
      >

      <div class="row bottom_download_section">
        <img
          src="../public/assets/download_ios.png"
          class="download_img col-6"
        />
        <img
          src="../public/assets/download_android.png"
          class="download_img col-6"
        />
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.bottom-container {
  background-color: #091527;
  height: auto;
  display: flex;
  align-items: center;
  justify-content: center;
}

.content-container {
  color: white;
  width: 70%;
  text-align: center;
  align-items: center;
  display: flex;
  flex-direction: column;
  padding: 0px 0px 40px 0px;
}

.bottom_span_info {
  font-size: 20px;
}

.download_img {
  width: 175px;
  margin: 0 50px;
}

.download_platform_button {
  color: #fff;
  background-color: #ea6923;
  border-radius: 20px;
  border: none;
  font-size: 20px;
  font-weight: 600;
  text-align: center;
  width: 550px;
}

.bottom_download_section {
  padding: 20px;
  width: 100%;
  justify-content: center;
}
</style>
