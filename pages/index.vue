<template>
  <div class="layout">
    <img src="~/assets/images/bg.png" alt="image" class="bg" />
    <div class="box-left">
      <span class="title">もっと おトク、 便利に !</span>
      <span class="sub mt-2"
        >OWNDAYSの会員サービス 『OWNDAYSメンバーシップ』</span
      >
    </div>
    <div class="box-right">
      <BoxRight
        :img="`${require('~/assets/images/icon-point.svg')}`"
        :text="'ポイントが 貯まる・使える'"
      />
      <BoxRight
        :img="`${require('~/assets/images/icon-friend.svg')}`"
        :text="'お友達紹介で どちらもおトク'"
      />

      <BoxRight
        :img="`${require('~/assets/images/icon-rank.svg')}`"
        :text="'ランクが上がると 還元率もアップ！'"
      />
      <BoxRight
        :img="`${require('~/assets/images/icon-mobile.svg')}`"
        :text="'会員だけが使える 便利でお得な機能'"
      />
    </div>

    <div
      class="row justify-content-between position-absolute box-right-ipad m-0"
    >
      <div class="col-3 p-0">
        <BoxRight
          :img="`${require('~/assets/images/icon-point.svg')}`"
          :text="'ポイントが 貯まる・使える'"
        />
        <BoxRight
          :img="`${require('~/assets/images/icon-rank.svg')}`"
          :text="'ランクが上がると 還元率もアップ！'"
        />
      </div>
      <div class="col-3 p-0">
        <BoxRight
          :img="`${require('~/assets/images/icon-friend.svg')}`"
          :text="'お友達紹介で どちらもおトク'"
        />
        <BoxRight
          :img="`${require('~/assets/images/icon-mobile.svg')}`"
          :text="'会員だけが使える 便利でお得な機能'"
        />
      </div>
    </div>
    <div class="box-bottom">
      <span class="text-white">サービス詳細・登録はこちら</span>
      <img
        src="~/assets/images/arrow-right.svg"
        alt="arrow-right"
        width="20px"
      />
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
@media only screen and (max-width: 800px) {
  .bg {
    height: 356px !important;
    object-fit: cover !important;
  }
  .box-right {
    display: none;
  }
  .box-bottom {
    display: none;
  }
  // .box-left {
  //   display: none;
  // }
}
.layout {
  overflow: hidden;
  height: 100vh;
  width: 100vw;
  position: relative;
}
.bg {
  width: 100%;
  height: auto;
  position: relative;
}
.box-right {
  top: 79px;
  left: 955px;
  position: absolute;
  display: flex;
  flex-wrap: wrap;
  width: 320px;
}
.box-right-ipad {
  display: flex;
  top: 0;
  width: 100%;
  @media only screen and (min-width: 799px) {
    display: none;
  }
}
.box-left {
  @media only screen and (max-width: 800px) {
    width: calc(100vw - 64px);
    height: 148px;
    left: 0;
    margin: 2rem;
    top: 176px;
    .title {
      text-align: center !important;
      font: normal normal normal 24px/32px Noto Sans JP !important;
      letter-spacing: 0.96px !important;
      width: auto !important;
    }
    .sub {
      text-align: center !important;
      font: normal normal normal 10px/29px Noto Sans JP !important;
      letter-spacing: 0.8px !important;
      color: #b6b6b6 !important;
    }
  }
  top: 105px;
  left: 140px;
  width: 350px;
  height: 350px;
  background: #000000 0% 0% no-repeat padding-box;
  border: 1px solid #ffffff;
  opacity: 1;
  position: absolute;
  padding: 2rem;
  .title {
    text-align: left;
    font: normal normal normal 44px/67px Noto Sans JP;
    letter-spacing: 1.88px;
    color: #ffffff;
    opacity: 1;
    width: 194px;
    display: block;
  }
  .sub {
    text-align: center;
    font: normal normal normal 17px/29px Noto Sans JP;
    letter-spacing: 1.36px;
    color: #ffffff;
    opacity: 1;
    display: block;
  }
}
.box-bottom {
  display: inline-block;
  text-align: center;
  padding-top: 31px;
  position: absolute;
  top: 400px;
  left: 958px;
  width: 310px;
  height: 83px;
  background: #516075 0% 0% no-repeat padding-box;
  opacity: 1;
  img {
    margin-left: 31px;
  }
}
</style>
