<template>
    <div class="step-container">
        <img :src="imgPath" class="step_img_background" />
        <div class="step_content">
            {{ content }}
        </div>
    </div>
</template>

<script>
export default {
  props: {
    imgPath: String,
    content: String,
  }
}
</script>


<style lang="scss">
.step-container {
    max-width: 600px;
    display: flex;
    justify-content: center;
}
.step_img_background {
    width: 300px;
}

.step_content {
    width: 225px;
    position: absolute;
    text-align: left;
    color: white;
    margin-top: 85px;
}
</style>
