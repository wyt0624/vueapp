<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input iconfont">
      <span class="iconfont">&#xe632;</span>
      输入城市景点游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right">
        城市
        <span class="iconfont arrow-icon">&#xe64a;</span>
      </div>
    </router-link>
  </div>
</template>
<script>
export default {
  name: "HomeHeader"
};
</script>
<style lang='stylus' scoped>
@import '~styles/varibles.styl';

.header {
  display: flex;
  line-height: 0.86rem;
  background: $bgColor;
  color: #fff;

  .header-left {
    width: 0.64rem;
    float: left;

    .back-icon {
      text-align: center;
      font-size: 0.4rem;
    }
  }

  .header-input {
    flex: 1;
    height: 0.64rem;
    line-height: 0.64rem;
    margin-top: 0.12rem;
    margin-left: 0.12rem;
    padding-left: 0.2rem;
    border-radius: 0.12rem;
    background: #fff;
    color: #ccc;
  }

  .header-right {
    width: 1.24rem;
    float: right;
    text-align: center;
    color: #fff

    .arrow-icon {
      font-size: 0.2rem;
      margin-left: -0.04rem;
    }
  }
}
</style>
