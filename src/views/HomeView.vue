<template>
  <div class="d-lg">
    <div class="header_contaner">
      <Header></Header>
      <NavBar></NavBar>
    </div>

    <Banner></Banner>
    <GamesList></GamesList>

    <div class="slot_container">
      <div class="slot_list">
        <div class="slot_item">
          <div class="logo">
            <img src="@/assets/mgshot.png" alt="" />
          </div>
          <div class="item_details">
            <span>MG SLOT</span>
            <span>E-Games</span>
          </div>
        </div>
        <div class="slot_item">
          <div class="logo">
            <img src="@/assets/jbdslot.png" alt="" />
          </div>
          <div class="item_details">
            <span>JBD SLOT</span>
            <span>E-Games</span>
          </div>
        </div>
      </div>
      <div>
        <img src="@/assets/matchbanner.png" alt="" />
        <button class="save_now">Bet now</button>
      </div>
    </div>

    <div class="entertainment_section_container">
      <div class="entertainment_section">
        <div>
          <img src="@/assets/girlimg.png" alt="" class="girl_img" />
        </div>
        <div class="entertainment_list">
          <div class="single_entertainment">
            <img src="@/assets/ent1.png" alt="" />
            <h3>AE LIVE</h3>
            <span>Live casino</span>
          </div>
          <div class="single_entertainment">
            <img src="@/assets/playent.png" alt="" />
            <h3>PP LIVE</h3>
            <span>Live casino</span>
          </div>
          <div class="single_entertainment">
            <h3>HUB-EVO</h3>
          </div>
          <div class="single_entertainment">
            <h3>ATMOSFERA</h3>
          </div>
          <div class="single_entertainment">
            <h3>TVBet</h3>
          </div>
          <div class="single_entertainment">
            <h3>VIVO LIVE</h3>
          </div>
        </div>
      </div>
    </div>

    <div class="sport_game_section">
      <div class="game_col">
        <img src="@/assets/sportimg1.jpg" alt="" class="img_margin" />
        <img src="@/assets/sportImg2.jpg" alt="" />
      </div>
      <div class="sport_center">
        <img src="@/assets/sportceterimg.png" alt="" />
      </div>
      <div class="game_col">
        <img src="@/assets/sportImg3.png" alt="" />
        <img src="@/assets/sportImg4.png" alt="" />
      </div>
    </div>

    <Footer></Footer>

    <div class="fixed_ads1"></div>
    <div class="fixed_ads2"></div>
    <div class="fixed_ads3"></div>
  </div>
  <MobileView></MobileView>
</template>

<script>
import Header from "@/components/Header.vue";
import NavBar from "@/components/NavBar.vue";
import Banner from "@/components/Banner.vue";
import GamesList from "@/components/GamesList.vue";
import Footer from "@/components/Footer.vue";
import MobileView from "./MobileView.vue";

export default {
  name: "HomeView",
  components: { Header, NavBar, Banner, GamesList, Footer, MobileView },
};
</script>

<style lang="scss" scoped>
.d-lg {
  display: block;
  @media (max-width: 1199px) {
    display: none;
  }
}
.header_contaner {
  background: url("@/assets/header_bg.png");
}
.slot_container {
  padding-bottom: 20px;
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  .slot_list {
    width: 422px;

    .slot_item {
      cursor: pointer;
      background-color: #100f0e;
      padding: 45px 0 47px 40px;
      display: flex;

      &:hover {
        background-color: #3a3a3a;
        .item_details {
          span {
            color: #e17f00;
          }
        }
      }
      .logo {
        width: 112px;
        margin-right: 30px;

        img {
          width: 100%;
        }
      }
      .item_details {
        display: flex;
        flex-direction: column;

        span:nth-child(1) {
          margin-bottom: 24px;
          font-size: 30px;
        }
        span:nth-child(2) {
          font-size: 16px;
        }
        span {
          font-style: italic;
          color: #cbcbcb;
        }
      }
    }
  }
  .save_now {
    display: block;
    margin: 0 auto;
    margin-top: 60px;
    width: 272px;
    text-align: center;
    line-height: 55px;
    font-style: italic;
    font-size: 22px;
    color: #ffcf51;
    cursor: pointer;
    background-image: url("@/assets/savenowimg.png");
    background-color: rgb(0, 0, 0);
  }
}
.entertainment_section_container {
  background-image: url("@/assets/entertainmentbg.png");
  background-size: cover;
  .entertainment_section {
    display: flex;
    justify-content: space-between;
    max-width: 1200px;
    margin: 0 auto;

    .girl_img {
      position: relative;
      transition: all 1s ease;
      right: 0;
      &:hover {
        right: -10px;
        cursor: pointer;
      }
    }
    .entertainment_list {
      display: flex;
      flex-wrap: wrap;
      .single_entertainment {
        width: 290px;
        height: 290px;
        cursor: pointer;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        color: #acacac;
        &:nth-child(odd) {
          background-color: #181717;
        }

        &:hover {
          background-color: transparent;
          background-image: url("@/assets/entbg.png");

          h3,
          span {
            color: #e17f00;
          }
        }
        h3 {
          color: #acacac;
          font-size: 40px;
          margin-bottom: 0;
        }
        span {
          font-size: 24px;
        }
      }
    }
  }
}
.sport_game_section {
  overflow: hidden;
  position: relative;
  max-width: 1200px;
  margin: 0 auto;
  height: 720px;
  display: flex;
  justify-content: space-between;

  .game_col {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
  }
  .sport_center {
    height: 100%;
    position: absolute;
    left: 50%;
    transform: translate(-50%);
    background-image: url("@/assets/sportceterbg.png");
    background-repeat: no-repeat;
  }
  .img_margin {
    margin-top: 70px;
  }
}

.fixed_ads1 {
  position: fixed;
  background-image: url("../assets/fixads.png");
  background-repeat: no-repeat;
  top: 0;
  width: 200px;
  height: 200px;
  right: 28px;
  top: 38%;
}
.fixed_ads2 {
  position: fixed;
  background-image: url("../assets/fixads1.png");
  background-repeat: no-repeat;
  top: 0;
  width: 200px;
  height: 200px;
  right: 28px;
  top: 68%;
}
.fixed_ads3 {
  position: fixed;
  background-image: url("../assets/fixads2.png");
  background-repeat: no-repeat;
  top: 0;
  width: 200px;
  height: 200px;
  left: 28px;
  top: 68%;
}
</style>
