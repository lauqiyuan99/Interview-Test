<template>
  <div class="container">
    <div class="title_container">
        Trading Guides
    </div>
    <div class="guide_container">
        <div class="guide_step_container">
            <Icon name="fluent:ios-arrow-left-24-regular" class="action_arrow_button left_button"/>

            <img src="../public/assets/guides_01.png" class="guide_img_background" />
            <div class="guide_step_content">
                Forex For Beginners
            </div>
        </div>
        <div class="guide_step_container">
            <img src="../public/assets/guides_02.png" class="guide_img_background" />
            <div class="guide_step_content">
                Analysing Made Easy
            </div>
        </div>
        <div class="guide_step_container">
            <Icon name="fluent:ios-arrow-right-24-regular" class="action_arrow_button right_button"/>
            <img src="../public/assets/guides_03.png" class="guide_img_background" />
            <div class="guide_step_content">
                CFDs Starter Kit
            </div>
        </div>
    </div>
  </div>
</template>



<style lang="scss">
.title_container {
    display: flex;
    justify-content: center;
    padding: 50px 0;
    font-size: 36px;
    color: #ea6923;
}

.guide_container {
    display: flex;
    justify-content: center;
}

.guide_step_container {
    position: relative;
    display: flex;
    justify-content: center;
    padding: 10px;
}

.action_arrow_button {
    position: absolute;
    color: #0477b5;
    background-color: rgba(0, 0, 0, 0.3 );;
    font-size: 30px;
    top: 50%;
    transform: translateY(-50%);
    height: 50px;
    border-radius: 5px;
}

.right_button {
    right: 10px;
    padding: 0 8px 0 0;
}

.left_button {
    left: 10px;
    padding: 0 0 0 8px;
}

.guide_img_background {
    width: 400px;
}

.guide_step_content {
    position: absolute;
    background-color: rgba(91.76%, 41.18%, 13.73%, 0.7);
    color: white;
    font-size: 16px;
    margin-bottom: 0;
    left: 10px;
    right: 10px;
    bottom: 20px;
    text-align: center;
    padding: 10px 0 5px 0;
}

</style>