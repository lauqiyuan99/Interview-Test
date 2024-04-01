<template>
  <div class="promotion-background pb-5 pt-2">
    <div class="container">
      <div class="border-first promo1Container">
        <div class="content mt-5">
          <div class="text">
            <div class="text left col ms-5">
              <div class="row mt-3">
                <div class="col-1">
                  <div
                    class="title-step d-flex justify-content-center step-number"
                  >
                    1
                  </div>
                </div>
                <div class="col-6">
                  <div class="description-title-step">US$200 credits</div>
                  <div class="description">
                    when you open an account & deposit US$200
                  </div>
                </div>
              </div>
              <div class="row mt-3">
                <div class="col-1">
                  <div
                    class="title-step d-flex justify-content-center step-number"
                  >
                    2
                  </div>
                </div>
                <div class="col-6">
                  <div class="description-title-step">US$20 credits</div>
                  <div class="description">
                    for every lot you trade, up to 20 lots
                  </div>
                </div>
              </div>
            </div>
            <div class="buttons" style="">
              <button class="buttons-text p-1">Create Live Account</button>
              <button class="buttons-text p-1">Download MI4 Platform</button>
            </div>
          </div>
          <div class="image">
            <img
              class="imgPromo1"
              src="../public/assets/Promo 1B.png"
              alt="Image"
            />
          </div>
        </div>
      </div>
    </div>
    <div class="container mt-5">
      <div class="border-second promo2Container">
        <div class="image">
          <img
            class="imgPromo2"
            src="../public/assets/Promo 2B.png"
            alt="Image"
          />
        </div>
        <div class="content mt-5">
          <div class="text right">
            <div class="text row">
              <div class="row mt-3">
                <div class="col-1">
                  <div
                    class="title-step d-flex justify-content-center step-number"
                  >
                    3
                  </div>
                </div>
                <div class="col-6">
                  <div class="description-title-step">
                    INR₹2000 Flipkart gift card
                  </div>
                  <div class="col">
                    <div class="description">
                      when you refer someone to enjoy
                    </div>
                    <div
                      class="title-step d-flex justify-content-center step-number"
                    >
                      1
                    </div>
                  </div>
                </div>
              </div>
              <div class="row mt-3">
                <div class="col-1">
                  <div
                    class="title-step d-flex justify-content-center step-number"
                  >
                    2
                  </div>
                </div>
                <div class="col-6">
                  <div class="description-title-step">
                    INR₹20,000 Flipkart gift card
                  </div>
                  <div class="row">
                    <div class="description">
                      When you refer a second person to enjoy
                    </div>
                    <div
                      class="title-step d-flex justify-content-center step-number me-1"
                    >
                      1
                    </div>
                    <div
                      class="title-step d-flex justify-content-center step-number me-1"
                    >
                      2
                    </div>
                    <div
                      class="title-step d-flex justify-content-center step-number me-1"
                    >
                      3
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="buttons-second">
              <button class="buttons-text p-1">Create Live Account</button>
              <button class="buttons-text p-1">Download MI4 Platform</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.promotion-background {
  background-color: #0477b5;
}

.promo1Container {
  margin-top: 100px;
}

.promo2Container {
  margin-top: 150px;
}

.border-first {
  position: relative;
  border: 2px solid #f68b1f;
  padding: 20px;
}

.border-first::after {
  content: "Free US$600 Credit!";
  font-size: 30px;
  position: absolute;
  top: -20px;
  left: 20%;
  transform: translateX(-50%);
  background-color: #0077b5;
  padding: 0 10px;
  color: #b9e6f9;
}
.border-second {
  position: relative;
  border: 2px solid #f68b1f;
  padding: 20px;
}

.border-second::after {
  content: "Free INR₹ 22,000 Gift Cards!";
  font-size: 30px;
  position: absolute;
  top: -20px;
  left: 65%;
  transform: translateX(-50%);
  background-color: #0077b5;
  padding: 0 10px;
  color: #b9e6f9;
}

.step-number {
  width: 25px;
  border-radius: 20px;
  background-color: #f68b1f;
}

.content {
  display: flex;
}

.text {
  flex: 1;
}

.text.right {
  margin-left: 700px;
}

.text.left {
  text-align: left;
}

.title-step {
  font-weight: 700;
  margin-bottom: 10px;
}

.description {
  margin-bottom: 10px;
  font-size: 15px;
  color: #b9e6f9;
}

.description-title-step {
  margin-bottom: 10px;
  color: #f68b1f;
  font-size: 15px;
  font-weight: 500;
}

.buttons {
  margin-top: 20px;
  margin-left: 100px;
  display: flex;
}

.buttons-second {
  display: flex;
  margin-top: 20px;
  margin-left: 50px;
  margin-right: 10px;
}

.buttons-second button {
  margin-right: 10px;
}

.buttons-text {
  background-image: linear-gradient(to top, #eb6b23, #f68a1e);
  color: #fff;
  border-radius: 20px;
  border: none;
  font-size: 10px;
  font-weight: 600;
  text-align: center;
}

.buttons button {
  margin-right: 10px;
}

.imgPromo1 {
  position: absolute;
  bottom: 0px;
  right: 200px;
  z-index: 1;
}

.imgPromo2 {
  position: absolute;
  bottom: 20px;
  left: 20px;
  z-index: 1;
}

.image img {
  max-width: calc(100% + 100px);
  max-height: calc(100% + 100px);
}
</style>
