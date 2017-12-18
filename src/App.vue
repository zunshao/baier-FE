<template>
  <div class = "" id="App">
    <top-nav></top-nav>
    <left-nav></left-nav>
    <foot-show></foot-show>
    <div class="view-container"></div>
  </div>
</template>

<script>
  import leftNav from '@/components/nav/leftNav'
  import topNav from '@/components/nav/topNav'
  import footShow from '@/components/footer/footShow'
export default {
  data() {
    return {
      key: ''
    }
  },
  props: [

  ],
  components: {
    leftNav,
    topNav,
    footShow

  },
  computed: {

  },
  mounted() {

  },
  methods: {

  }
}
</script>

<style>
@import "assets/styles/main.less";
  .view-container{
    width: 80.7vw;
    height: 82vh;
    margin-top: 1vh;
    margin-right: 1.3vw;
    background: aquamarine;
    float: right;
    border-radius: .5rem;
  }
</style>
