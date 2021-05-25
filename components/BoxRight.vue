<template>
  <div class="box-content">
    <img :src="img" alt="" />
    <div>
      {{ text }}
    </div>
  </div>
</template>

<script>
export default {
  props: ["img", "text"]
};
</script>

<style lang="scss" scoped>
.box-content {
  background: #ffffff 0% 0% no-repeat padding-box;
  opacity: 1;
  width: 150px;
  height: 150px;
  text-align: center;
  padding: 1.4rem;
  margin: 0.25rem;
  img {
    padding-bottom: 1;
  }
  div {
    text-align: center;
    font: normal normal bold 13px/19px Noto Sans JP;
    letter-spacing: 0.56px;
    color: #000000;
    opacity: 1;
    width: 109px;
  }
}
@media only screen and (max-width: 1399px) {
  .box-content {
    margin: 1rem;
    width: 80px;
    height: 80px;
    padding: 0.25rem;
    padding-top: 1rem;
    img {
      padding-bottom: 0.4rem;
      width: 30px;
    }
    div {
      text-align: center;
      font: normal normal bold 7px/9px Noto Sans JP;
      letter-spacing: 0.28px;
      width: 100%;
    }
  }
}
</style>
