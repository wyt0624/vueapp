<template>    
    <div class="city-header">
        城市选择
        <router-link to="/">
            <div class="iconfont back-icon">&#xe624;</div>
        </router-link>
        
    </div>
</template>
<script>
export default {
    name: "CityHeader"
}
</script>
<style lang="stylus" scoped>
@import "~styles/varibles.styl";
    .city-header
        position: relative
        overflow: hidden
        text-align: center
        line-height: 0.86rem
        color: #fff
        background: $bgColor
        font-size: .32rem
        .back-icon
           position: absolute
           width: .64rem
           font-size: .32rem
           text-align: center
           color: #fff
           top: 0
           left: 0
</style>