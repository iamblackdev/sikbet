<template>
  <div class="mobile_view">
    <div class="header">
      <div class="notification">
        <img src="@/assets/beIlicon.png" alt="" />
        <div class="badge">5</div>
      </div>
      <img src="@/assets/mobileLogo.png" alt="" class="mobile_logo" />
      <div class="hamburger">
        <img
          src="@/assets/hamburger.png"
          alt=""
          @click="dhowDropDown = !dhowDropDown"
        />
      </div>
      <div class="dropdown" v-show="dhowDropDown">
        <div class="dropdown_item">
          <img src="@/assets/philipine.png" alt="" />
          <span>हिंदी</span>
        </div>
        <div class="dropdown_item">
          <img src="@/assets/facebook.png" alt="" />
          <span>Facebook</span>
        </div>
        <div class="dropdown_item">
          <img src="@/assets/instagram.png" alt="" />
          <span>Ins</span>
        </div>
        <div class="dropdown_item">
          <img src="@/assets/youtube.png" alt="" />
          <span>Youtube</span>
        </div>
        <div class="dropdown_item">
          <img src="@/assets/telegram.png" alt="" />
          <span>Telegram</span>
        </div>
      </div>
    </div>

    <div class="carousel">
      <a-carousel>
        <div>
          <img class="carousel_image" src="@/assets/mobilebannerImg1.jpg" alt />
        </div>
        <div>
          <img class="carousel_image" src="@/assets/mobilebannerImg2.jpg" alt />
        </div>
      </a-carousel>
    </div>

    <div class="hot_games">
      <p>Hot Game</p>

      <div class="game_list">
        <div class="game">
          <img src="@/assets/game1.jpg" alt="" />
        </div>
        <div class="game">
          <img src="@/assets/game2.jpg" alt="" />
        </div>
        <div class="game">
          <img src="@/assets/game3.jpg" alt="" />
        </div>
        <div class="game">
          <img src="@/assets/game4.jpg" alt="" />
        </div>
        <div class="game">
          <img src="@/assets/game5.jpg" alt="" />
        </div>
        <div class="game">
          <img src="@/assets/game6.jpg" alt="" />
        </div>
      </div>
    </div>
    <div class="bottom_widget">
      <div class="top">
        <div class="user">
          <img src="@/assets/userIcon.png" alt="" />
          <div class="details">
            <span>Welcome</span>
            <span>Please login !</span>
          </div>
        </div>
      </div>
      <div class="body">
        <div class="side_bar">
          <div class="img_wrapper">
            <img src="@/assets/mplaybtn.png" alt="" />
          </div>
          <div class="img_wrapper">
            <img src="@/assets/msidebar2.png" alt="" />
          </div>
          <div class="img_wrapper">
            <img src="@/assets/msidebar3.png" alt="" />
          </div>
          <div class="img_wrapper">
            <img src="@/assets/msidebar4.png" alt="" />
          </div>
          <div class="img_wrapper">
            <img src="@/assets/msidebar5.png" alt="" />
          </div>
          <div class="img_wrapper">
            <img src="@/assets/msidebar6.png" alt="" />
          </div>
        </div>
        <div class="content">
          <div class="content_image_wrapper">
            <img src="@/assets/smc1.png" alt="" />
          </div>
          <div class="content_image_wrapper">
            <img src="@/assets/smc2.png" alt="" />
          </div>
          <div class="content_image_wrapper">
            <img src="@/assets/smc3.jpg" alt="" />
          </div>
          <div class="content_image_wrapper">
            <img src="@/assets/smc4.jpg" alt="" />
          </div>
          <div class="content_image_wrapper">
            <img src="@/assets/smc5.jpg" alt="" />
          </div>
          <div class="content_image_wrapper">
            <img src="@/assets/smc6.png" alt="" />
          </div>
          <div class="content_image_wrapper">
            <img src="@/assets/smc7.png" alt="" />
          </div>
          <div class="content_image_wrapper">
            <img src="@/assets/smc8.png" alt="" />
          </div>
        </div>
      </div>
    </div>

    <div class="fixed_mobile_nav">
      <div class="tab_icon">
        <img src="@/assets/fht1.png" alt="" />
      </div>
      <div class="tab_icon">
        <img src="@/assets/fht2.png" alt="" />
      </div>
      <div class="tab_icon">
        <img src="@/assets/fht3.png" alt="" />
      </div>
      <div class="tab_icon">
        <img src="@/assets/fht.png" alt="" />
      </div>
      <div class="tab_icon">
        <img src="@/assets/fht5.png" alt="" />
      </div>
    </div>
    <div class="fix_ads">
      <img src="@/assets/mfi1.png" alt="" width="50px" />
      <img src="@/assets/mfi2.png" alt="" width="50px" />
      <img src="@/assets/mfi3.png" alt="" width="50px" />
    </div>
  </div>
</template>

<script>
export default {
  name: "MobileView",

  data() {
    return {
      dhowDropDown: false,
    };
  },
};
</script>

<style lang="scss" scoped>
.mobile_view {
  display: block;
  color: #cbcbcb !important;
  width: 100%;
  height: 100%;
  background-color: #1a1a1a;
  min-height: 100vh;

  @media (min-width: 1200px) {
    display: none;
  }

  .header {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-shrink: 0;
    padding: 0 3.2vw;
    height: 12.26667vw;

    .notification {
      position: relative;
      img {
        width: 30px;
      }
      .badge {
        position: absolute;
        top: 0;
        right: 0;
        display: flex;
        align-items: center;
        justify-content: center;
        min-width: 4.26667vw;
        padding: 0 0.8vw;
        font-weight: 500;
        font-size: 3.2vw;
        font-family: -apple-system-font, Helvetica Neue, Arial, sans-serif;
        line-height: 1.2;
        background-color: #ee0a24;
        border: 0 solid #fff;
        border-radius: 266.4vw;
      }
    }

    .mobile_logo {
      width: 100px;
    }
    .hamburger {
      width: 20px;
      img {
        width: 100%;
      }
    }
  }
  .carousel {
    height: 40vw;
    flex-shrink: 0;
    margin: 0px 3.2vw;
    overflow: hidden;
    border-radius: 8px;

    .carousel_image {
      width: 100%;
      vertical-align: middle;
    }
  }
  .hot_games {
    background: #303032;
    margin: 2.13333vw 3.2vw;
    border-radius: 2.13333vw;
    p {
      color: #ebd193;
      font-size: 3.73333vw;
      padding: 2.66667vw 0 0 2.66667vw;
      margin-bottom: 0px;
    }
    .game_list {
      padding: 2.66667vw 0;
      display: flex;
      overflow-x: scroll;

      .game {
        height: 16vw;
        min-width: 16vw;
        margin-left: 2.66667vw;
        border: 1px solid #2d2c2a;
        img {
          width: 100%;
        }
      }
    }
  }
  .bottom_widget {
    background: #303032;
    margin: 0 3.2vw;
    border-radius: 2.13333vw;
    flex-grow: 1;
    display: flex;
    flex-direction: column;

    .card_top {
      display: flex;
      align-items: center;
      height: 16vw;
      border-bottom: 1px solid #1e1e1e;
      margin: 0 3.2vw;
    }
  }
  .top {
    display: flex;
    align-items: center;
    height: 16vw;
    border-bottom: 1px solid #1e1e1e;
    margin: 0 3.2vw;
    .user {
      display: flex;
      align-items: flex-end;

      img {
        width: 6vw;
        margin-right: 2vw;
      }
      .details {
        display: flex;
        flex-direction: column;

        span:nth-child(1) {
          font-size: 3.73333vw;
          color: #8b8780;
        }
        span:nth-child(2) {
          font-size: 3.73333vw;
          color: #ebd193;
          text-decoration: underline;
          line-height: 1;
        }
      }
    }
  }
  .body {
    display: flex;
    padding: 3.2vw 3.2vw 0 3.2vw;
    flex-grow: 1;
    .side_bar {
      height: 90.66667vw;
      overflow-x: hidden;
      overflow-y: scroll;
      padding-right: 5.2vw;
      .img_wrapper {
        margin-top: 3.2vw;
        width: 13.33333vw;
        height: 13.33333vw;

        &:first-child {
          margin-top: 0;
        }

        img {
          width: 100%;
        }
      }
    }
    .content {
      width: fit-content;
      height: 90.66667vw;
      overflow-x: hidden;
      overflow-y: scroll;

      .content_image_wrapper {
        height: 18.4vw;
        width: 70.66667vw;
        height: 18.4vw;
        margin-bottom: 1.86667vw;
        border-radius: 6px;
        img {
          width: 100%;
          height: 100%;
        }
      }
    }
  }
  .fixed_mobile_nav {
    position: fixed;
    bottom: 2.66667vw;
    border-radius: 13.33333vw;
    width: 93.33333vw;
    box-shadow: 1px 0 1.06667vw 1px #1a1a1a;
    background-color: #303032;
    border-radius: 13.33333vw;
    display: flex;
    align-items: center;
    left: 50%;
    transform: translate(-50%);
    .tab_icon {
      display: flex;
      align-items: center;
      justify-content: center;
      height: 13.33333vw;
      width: 18vw;
      img {
        height: 5.33333vw;
      }
    }
  }
  .fix_ads {
    position: fixed;
    right: 0px;
    bottom: 130px;
    display: flex;
    flex-direction: column;
  }
  .dropdown {
    z-index: 32;
    position: absolute;
    top: 45px;
    right: 0;
    background-color: rgba(0, 0, 0, 0.8);
    overflow: hidden;
    border-radius: 2.13333vw;
    font-size: 3.2vw;
    padding: 0 2.66667vw;

    .dropdown_item {
      padding: 2.66667vw 0;
      display: flex;
      justify-content: flex-start;
      align-items: center;

      img {
        margin-right: 2.66667vw;
        width: 5.33333vw;
      }

      &:first-child {
        border-bottom: 1px solid #ebedf0;
      }
    }
  }
}
</style>
