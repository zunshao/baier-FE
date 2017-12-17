<template>
  <div class = "" id="App">
    <top-nav></top-nav>
    <left-nav></left-nav>
    <foot-show></foot-show>
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
@import "./assets/styles/main.css";
</style>
