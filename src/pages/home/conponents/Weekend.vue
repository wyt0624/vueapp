<template>
    <div>
       <div class="recommend-title">周末游</div>

        <div class="item border-bottom" v-for="item of list" :key="item.id">
            <div>
                <img class="item-img" :src="item.imgUrl" />
            </div>
             <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
             </div>

           
            

        </div>
    </div>
</template>
<script>
export default {
    name: "HomeWeekend",
    props: {
        list: Array
    },
    data() {
        return {
            recommendList:[{
                id: "0001",
                imgUrl: "http://img1.qunarzz.com/sight/p0/1902/84/84696f368bbec10da3.img.jpg_200x200_50323152.jpg",
                title: "世界园艺博览会",
                desc: "世界园艺博览会世界园艺博览会世界园艺博览会"
            },{
                id: "0002",
                imgUrl: "http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_200x200_1bc99086.jpg",
                title: "故宫",
                desc: "世界五大宫之首，穿越与您近在咫尺"
            },{
                id: "0003",
                imgUrl: "http://img1.qunarzz.com/sight/p0/1708/2b/2b3b94de99c0a425a3.img.jpg_200x200_2458ffb2.jpg",
                title: "八达岭长城",
                desc: "不到长城非好汉"
            },{
                id: "0004",
                imgUrl: "http://img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_200x200_99ae30ee.jpg",
                title: "北京欢乐谷",
                desc: "北京欢乐谷"
            },]
        }
    },
}
</script>
<style lang='stylus' scoped>
@import '~styles/mixins.styl';
    .recommend-title
        margin-top: .2rem
        line-height: .8rem
        background-color: #eee
        text-indent: .2rem 
    .item
        overflow: hidden
        height: 4rem
        .item-img
            width: 100%
            height: 2.5rem
            padding: .1rem
        .item-info
            flex: 1
            padding: .1rem
            min-width: 0
            height: .8rem
            padding: .14rem .2rem .2rem .2rem
            .item-title
                line-height: .54rem
                font-size: .26rem
                ellipsis()
            .item-desc
                line-height: .4rem
                color: #ccc
                ellipsis()
        
</style> 

