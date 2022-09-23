<template>
  <div class="app_nav_bar_container">
    <div class="app_nav_bar">
      <router-link to="/download" class="app_download"
        >APP DOWNLOAD</router-link
      >
      <router-link to="/" class="home"
        ><img src="@/assets/homeImg.png" alt="" />
        <span>HOME</span></router-link
      >
      <router-link to="/live-casino">
        <img src="@/assets/livecasino.png" alt="" />
        <span>LIVECASINO</span></router-link
      >
      <router-link to="/sport-game">
        <img src="@/assets/sports.png" alt="" />
        <span>SPORTS</span>
      </router-link>
      <router-link to="/lottery">
        <img src="@/assets/lottery.png" alt="" />
        <span>LOTTERY</span>
      </router-link>
      <router-link to="/teenpatti">
        <img src="@/assets/tennpatti.png" alt="" />
        <span>TEEN PATTI</span>
      </router-link>
      <router-link to="/chess-cards">
        <img src="@/assets/cardgame.png" alt="" />
        <span>CARDGAME</span>
      </router-link>

      <router-link to="/e-game">
        <img src="@/assets/slot.png" alt="" />
        <span>SLOT</span>
      </router-link>
      <router-link to="/promotions">
        <img src="@/assets/promotion.png" alt="" />
        <span>PROMOTION</span>
      </router-link>
      <router-link to="/customers">
        <img src="@/assets/customer.png" alt="" />
        <span>CUSTOMERS</span>
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",

  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.app_nav_bar_container {
  height: 53px;
  border-top: 2px solid #efb158;

  .app_nav_bar {
    display: flex;
    margin: 0 auto;
    max-width: 1200px;

    .app_download {
      background-color: rgb(62, 61, 61);
    }

    display: flex;

    a {
      width: 166px;
      height: 51px;
      font-family: 黑体;
      font-size: 16px;
      color: rgb(226, 226, 226);
      white-space: nowrap;
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      align-items: center;
      img {
        display: none;
        margin-right: 5px;
      }

      &:hover {
        background-color: rgb(62, 61, 61);
        img {
          display: block;
        }
      }
    }
    .router-link-exact-active {
      background-color: #bc891f;
      img {
        display: block;
      }
    }
  }
}
</style>
