<template>
  <div class="app_footer">
    <div class="footer_links">
      <span>About us</span>
      <span>Contact us</span>
      <span>Partnership</span>
      <span>Help with deposits and withdrawals</span>
      <span>Q&A</span>
    </div>
    <div class="footer_img"></div>
    <p class="copy_write">Copyright @ Sikwin Reserved</p>
  </div>
</template>

<script>
export default {
  name: "Footer",

  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.app_footer {
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 1200px;
  margin: 0 auto;
  font-size: 16px;
  padding: 30px 0 20px 0;
  .footer_links {
    display: flex;
    span {
      padding: 0 34px;
      border-right: 1px solid #b4b5b7;
      cursor: pointer;
      color: #bcbcbc;

      &:last-child {
        border-right: 0;
      }
    }
  }
  .footer_img {
    background-image: url("@/assets/footerimg.png");
    height: 52px;
    width: 100%;
    margin: 30px auto 0;
  }
  .copy_write {
    text-align: center;
    color: #7b7b7b;
    text-align: center;
    margin-top: 25px;
  }
}
</style>
