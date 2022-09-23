<template>
  <div class="app_game_list_conteiner">
    <div class="game_list">
      <div class="game_type">
        <img src="@/assets/match.png" alt="" />
        <span class="tag">Sports</span>
        <div class="hover_bg">
          <span>PLAY FOR SPORTS</span>
        </div>
      </div>
      <div class="game_type">
        <img src="@/assets/entertainment.png" alt="" />
        <span class="tag">Live casino</span>
        <div class="hover_bg">
          <span>PLAY FOR LIVE</span>
        </div>
      </div>
      <div class="game_type">
        <img src="@/assets/electronic.png" alt="" />
        <span class="tag">E-Games</span>
        <div class="hover_bg">
          <span>PLAY FOR E-GAMES</span>
        </div>
      </div>
      <div class="game_type">
        <img src="@/assets/animal.png" alt="" />
        <span class="tag">Chess games</span>
        <div class="hover_bg">
          <span>PLAY FOR CHESS</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "GameList",

  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.app_game_list_conteiner {
  background-image: url(/src/assets/rocky-bg.png);
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;

  width: 100%;
  height: 419px;

  .game_list {
    max-width: 1200px;
    margin: 0 auto;
    padding-top: 30px;
    display: flex;
    justify-content: space-between;
    .game_type {
      position: relative;
      cursor: pointer;
      width: 267px;
      height: 330px;
      position: relative;

      .hover_bg {
        display: none;
      }
      &:hover {
        .hover_bg {
          display: flex;
          position: absolute;
          top: 0;
          width: 100%;
          height: 100%;
          background: rgba(0, 0, 0, 0.5);
          left: 0px;
          align-items: center;
          justify-content: center;

          span {
            background-image: url("@/assets/playbagembg.png");
            width: 202px;
            line-height: 51px;
            text-align: center;
            font-size: 16px;
            font-family: Adobe Heiti Std;
            color: #ebc86d;
          }
        }
      }

      .tag {
        z-index: 2;
        position: absolute;
        bottom: -36px;
        right: 0;
        display: flex;
        text-align: center;
        align-items: center;
        justify-content: center;
        background-image: url("@/assets/gametypebg.png");
        width: 143px;
        height: 51px;
        font-size: 19px;
        color: #712213;
        font-style: italic;
        padding-left: 15px;
      }
    }
  }
}
</style>
