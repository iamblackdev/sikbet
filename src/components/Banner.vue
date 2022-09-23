<!--  -->
<template>
  <div class="app_banner">
    <div class="carousel">
      <a-carousel centerPadding="100px" arrows>
        <template #prevArrow>
          <div class="custom-slick-arrow" style="left: 10px; z-index: 1">
            <left-circle-outlined />
          </div>
        </template>
        <template #nextArrow>
          <div class="custom-slick-arrow" style="right: 10px">
            <right-circle-outlined />
          </div>
        </template>

        <div>
          <img class="carousel_image" src="@/assets/bannerImg1.jpg" alt />
        </div>
        <div>
          <img class="carousel_image" src="@/assets/bannerImg2.jpg" alt />
        </div>
      </a-carousel>
    </div>
  </div>
</template>

<script>
import { LeftCircleOutlined, RightCircleOutlined } from "@ant-design/icons-vue";
export default {
  name: "Banner",
  components: { LeftCircleOutlined, RightCircleOutlined },
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.app_banner {
  max-height: 398px;
  min-height: 248px;
  box-shadow: inset 0 0 16px 4px #000;
  background-color: #000;
  background-image: linear-gradient(45deg, #141414 25%, transparent 0),
    linear-gradient(-45deg, #141414 25%, transparent 0),
    linear-gradient(45deg, transparent 75%, #141414 0),
    linear-gradient(-45deg, transparent 75%, #141414 0);
  background-size: 18px 18px;
  overflow: hidden;
}

.carousel_image {
  width: 100%;
  height: 389px;
  vertical-align: middle;
}

.ant-carousel :deep(.slick-arrow.custom-slick-arrow) {
  width: 25px;
  height: 25px;
  font-size: 25px;
  color: #fff;
  background-color: rgba(31, 45, 61, 0.11);
  opacity: 0.3;
  z-index: 1;
}
.ant-carousel :deep(.custom-slick-arrow:before) {
  display: none;
}
.ant-carousel :deep(.custom-slick-arrow:hover) {
  opacity: 0.5;
}
</style>
