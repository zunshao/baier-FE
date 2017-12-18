<template>
  <div class = "topNav">
    <div class="logo">
      LOGO
    </div>
    <ul class="nav-show">
      <li class="nav-active"><Icon type="ios-navigate" />平台管理</li>
      <li><Icon type="ios-keypad" />admin</li>
      <li><Icon type="ios-analytics"></Icon> 意见建议</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      key: ''
    }
  },
  props: [

  ],
  components: {

  },
  computed: {

  },
  mounted() {

  },
  methods: {

  }
}
</script>

<style scoped lang="less">
  @topHeight: 9vh;
  .topNav{
    width: 100vw;
    height: @topHeight;
    line-height: @topHeight;
    background: linear-gradient(90deg, #445dd1, #3298ff);
    overflow: hidden;
  }
  .logo{
    height: inherit;
    line-height: inherit;
    width: 3rem;
    margin-left: .5rem;
    font-weight: bold;
    color: #fff;
    float: left;
  }
  .nav-show{
    overflow: hidden;
    float: right;
    margin-right: 12rem;
    .nav-active{
      olor: #fff;
    }
  }
  .nav-show li{
    display: inline-block;
    float: left;
    width: fit-content;
    font-size: 1.1rem;
    color: #eee;
    margin-right: 2rem;
    cursor: pointer;
    font-weight: 500;
    transition: all .2s ease-in-out;
    &:hover{
      color: #fff;
      transition: all .2s ease-in-out;
    }
    &:last-child{
      margin-right: 0;
    }
    i{
      margin-right: .5rem;
    }
  }
</style>
