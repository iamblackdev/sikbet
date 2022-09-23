<template>
  <div class="app_header">
    <div class="header_images">
      <img src="@/assets/youtube.png" alt="yotube" />
      <img src="@/assets/instagram.png" alt="instagram" />
      <img src="@/assets/facebook.png" alt="faceboook" />
      <img src="@/assets/telegram.png" alt="telegram" />
      <div class="logo"></div>
    </div>
    <div class="aside_btn">
      <button class="login">Login</button>
      <button class="sign_up">Sign-up</button>
      <div class="language">
        <div class="language_select_btn" @click="showLangList = !showLangList">
          <img :src="selectedLang.imgUrl" alt="" />
          {{ selectedLang.name }}
          <img src="@/assets/arrowDown.png" alt="" />
        </div>
        <ul v-show="showLangList" class="laguage_list">
          <li
            v-for="lang in languages"
            :key="lang.name"
            @click="selectedLang = lang"
          >
            <img :src="lang.imgUrl" :alt="lang.name" />
            {{ lang.name }}
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import englishImg from "@/assets/usa.png";
import philipine from "@/assets/philipine.png";
export default {
  name: "Header",

  data() {
    return {
      selectedLang: { name: "English", imgUrl: englishImg },
      languages: [
        { name: "हिंदी", imgUrl: philipine },
        { name: "English", imgUrl: englishImg },
      ],
      showLangList: false,
    };
  },
};
</script>

<style lang="scss" scoped>
.app_header {
  max-width: 1200px;
  margin: 0 auto;
  padding: 15px 0;
  display: flex;
  align-items: center;
  justify-content: space-between;

  .header_images {
    display: flex;
    align-items: center;
    img {
      width: 30px;
      margin-right: 18px;

      &:last-child {
        margin-right: 0;
      }
    }
    .logo {
      width: 240px;
      height: 40px;
      background: url("@/assets/appLogo.png") no-repeat;
      background-size: 100% 100%;
      background-size: contain;
      cursor: pointer;
    }
  }
  .aside_btn {
    display: flex;
    button {
      border-radius: 6px;
      width: 94px;
      height: 34px;
      font-size: 16px;
      color: #fff;
      text-align: center;
      line-height: 34px;
      margin-right: 20px;
      cursor: pointer;
    }
    .login {
      background-color: #c33030;
    }
    .sign_up {
      background-color: #d6a22a;
    }
    .language {
      cursor: pointer;
      position: relative;
      color: #e1e1e1;
      font-size: 14px;
      .language_select_btn {
        width: 132px;
        height: 30px;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding-left: 15px;
        border-left: 1px solid #8c8c8c;
      }
      .laguage_list {
        background: #3c3c3c;
        border-radius: 8px;
        position: absolute;
        top: 32px;
        right: 0;
        z-index: 2;

        li {
          display: flex;
          align-items: center;
          padding: 0 7px;
          margin: 5px 0;
          font-size: 13px;
          line-height: 30px;

          img {
            margin-right: 5px;
          }

          &:hover {
            background: #636363;
          }
        }
      }
    }
  }
}
</style>
