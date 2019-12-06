<template>
  <div class="home">
      <div class="banner">
        <swiper :options='swiperOption' ref="mySwiper">
          <swiper-slide class="item">1</swiper-slide>
          <swiper-slide class="item">2</swiper-slide>
          <swiper-slide class="item">3</swiper-slide>
          <swiper-slide class="item">4</swiper-slide>
        </swiper>
      </div>
      <div class="ListItem"> 
        <div class="Item_List" v-for="(item,key) in List" :key="key">
          <dl>
            <dt><img :src="item.image" alt=""></dt>
            <dd>{{item.title}}</dd>
          </dl>
        </div>
      </div>
  </div>
</template>

<script>
export default {
  name:'',
  data () {
    return {
      swiperOption:{
        loop:true,
        autoplay:true
      },
      List:[
        {title:'成单奖励',image:'http://hiphotos.baidu.com/feed/pic/item/b17eca8065380cd7092d50f2ab44ad34598281fa.jpg',id:1},
        {title:'成单奖励',image:'http://hiphotos.baidu.com/feed/pic/item/b17eca8065380cd7092d50f2ab44ad34598281fa.jpg',id:2},
        {title:'成单奖励',image:'http://hiphotos.baidu.com/feed/pic/item/b17eca8065380cd7092d50f2ab44ad34598281fa.jpg',id:3},
        {title:'成单奖励',image:'http://hiphotos.baidu.com/feed/pic/item/b17eca8065380cd7092d50f2ab44ad34598281fa.jpg',id:4},
        {title:'成单奖励',image:'http://hiphotos.baidu.com/feed/pic/item/b17eca8065380cd7092d50f2ab44ad34598281fa.jpg',id:5},
        {title:'成单奖励',image:'http://hiphotos.baidu.com/feed/pic/item/b17eca8065380cd7092d50f2ab44ad34598281fa.jpg',id:6},
        {title:'成单奖励',image:'http://hiphotos.baidu.com/feed/pic/item/b17eca8065380cd7092d50f2ab44ad34598281fa.jpg',id:7},
        {title:'成单奖励',image:'http://hiphotos.baidu.com/feed/pic/item/b17eca8065380cd7092d50f2ab44ad34598281fa.jpg',id:8},
      ]
    };
  },

  components: {},

  computed: {
    swiper(){
      return this.$refs.mySwiper.swiper
    }
  },
//方法
  methods: {}
}

</script>
<style lang='scss' scoped>
.item{
  width: 100%;
  height: 200px;
  text-align: center;
  line-height: 200px;
}
.ListItem{
  width: 100%;
  display: flex;
  flex-wrap: wrap;
}
.Item_List{
  flex-shrink: 0;
  width: 20%;
  height: 100px;
  margin: 10px 2.5%;
  dt{
    width: 70px;
    height: 70px;
    border-radius: 50%;
    overflow: hidden;
    img{
      width: 100%;

    }
  }
  dd{
    width: 100%;
    text-align: center;
    line-height: 30px;
    font-size: 16px;
  }
}
</style>
