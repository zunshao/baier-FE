<style>
@import "./assets/styles/main.css";
.layout {
  border: 1px solid #d7dde4;
  background: #f5f7f9;
}
.ivu-menu-dark {
  background: linear-gradient(90deg, #445dd1, #3298ff);
}
.ivu-menu-horizontal {
  height: 4rem;
  line-height: 4rem;
}
.layout-logo {
  width: 10rem;
  height: 2rem;
  float: left;
  position: relative;
  top: 1rem;
  left: 1.6rem;
  text-align: left;
  line-height: 2rem;
  font-weight: bold;
  color: #fff;
}
.layout-nav {
  width: fit-content;
  float: right;
  margin-right: 14rem;
}
.layout-assistant {
  width: 300px;
  margin: 0 auto;
  height: inherit;
}
.layout-breadcrumb {
  padding: 10px 15px 0;
}
.layout-content {
  min-height: 200px;
  margin: 15px;
  overflow: hidden;
  background: #fff;
  border-radius: 4px;
}
.layout-content-main {
  padding: 10px;
}
.layout-copy {
  text-align: center;
  padding: 10px 0 20px;
  color: #9ea7b4;
}
</style>
<template>
  <div class="layout" id="app">
    <Menu mode="horizontal" theme="dark">
      <div class="layout-logo">LOGO</div>
      <div class="layout-nav">
        <li
          class="ivu-menu-item"
          v-for="(item, index) in topNavData"
          :key="item.name"
          v-bind:class="[{'ivu-menu-item-active ivu-menu-item-selected': topNav.active === index}]"
          @click="topNavClick(index)">
          <Icon :type="item.icon"></Icon>
          {{ item.content + ':' + index}}
        </li>
      </div>
    </Menu>
    <!--<div class="layout-content">
      <Row>
        <Col span="5">
        <Menu active-name="1-2" width="auto" :open-names="['1']">
          <Submenu name="1">
            <template slot="title">
              <Icon type="ios-navigate"></Icon>
              Item 1
            </template>
            <MenuItem name="1-1">Option 1</MenuItem>
            <MenuItem name="1-2">Option 2</MenuItem>
            <MenuItem name="1-3">Option 3</MenuItem>
          </Submenu>
          <Submenu name="2">
            <template slot="title">
              <Icon type="ios-keypad"></Icon>
              Item 2
            </template>
            <MenuItem name="2-1">Option 1</MenuItem>
            <MenuItem name="2-2">Option 2</MenuItem>
          </Submenu>
          <Submenu name="3">
            <template slot="title">
              <Icon type="ios-analytics"></Icon>
              Item 3
            </template>
            <MenuItem name="3-1">Option 1</MenuItem>
            <MenuItem name="3-2">Option 2</MenuItem>
          </Submenu>
        </Menu>
        </Col>
        <Col span="19">
        <div class="layout-content-main">Content</div>
        </Col>
      </Row>
    </div>-->
    <div class="layout-copy">
      2011-2016 &copy; TalkingData
    </div>
  </div>
</template>
<script>
export default {
  name: "app",
  data: () => ({
    topNav: {
      active: 0
    },
    topNavData: [
      {
        name: 1,
        icon: "ios-navigate",
        content: "topItem1",
        child: []
      },
      {
        name: 2,
        icon: "ios-keypad",
        content: "topItem2",
        child: []
      },
      {
        name: 3,
        icon: "ios-analytics",
        content: "topItem3",
        child: []
      },
      {
        name: 4,
        icon: "ios-paper",
        content: "topItem4",
        child: []
      }
    ]
  }),
  methods: {
    topNavClick: function(index) {
      this.topNav.active = index;
    }
  }
};
</script>
