<template>
<div class="drawer apps" v-click-outside="closeLeftMenu" v-bind:class="{ active: showLeftMenu }" v-on:click="showLeftMenu=true">
  <div class="icon">
    <Icon type="md-apps" size="18" />
  </div>
  <transition name="custom-classes-transition" enter-active-class="animated slideInLeft faster">
    <div class="left-bar" v-show="showLeftMenu">
      <a href="/" class="app" :key="item.id" v-for="item in items">
          <Icon class="icon" type="md-square-outline" />
          <div class="name">{{item.name}}</div>
        </a>
    </div>
  </transition>
</div>
</template>

<script>
import ClickOutside from "../directives/clickoutside";
export default {
  name: "leftmenu",
  directives: {
    ClickOutside
  },
  data() {
    return {
      showLeftMenu: false,
      items: [{
          id: 1,
          name: "发文"
        },
        {
          id: 2,
          name: "发文"
        },
        {
          id: 3,
          name: "发文"
        },
        {
          id: 4,
          name: "发文"
        },
        {
          id: 5,
          name: "发文"
        },
        {
          id: 6,
          name: "发文"
        },
        {
          id: 7,
          name: "发文"
        },
        {
          id: 8,
          name: "发文"
        },
        {
          id: 9,
          name: "发文"
        }
      ]
    };
  },
  methods: {
    closeLeftMenu() {
      this.showLeftMenu = false;
    }
  }
};
</script>

<style lang="scss" scoped>
.left-bar {
  position: absolute;
  display: none;
  top: 48px;
  left: 0;
  bottom: 0;
  width: 320px;
  background: #ffffff;
  box-shadow: rgba(0, 0, 0, 0.2) 30px 0px 30px -30px;
  padding: 23px 18px 0 23px;
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-start;
  align-content: flex-start;
  z-index: 9999;

  .app {
    background: #f8f8f8;
    width: 88px;
    height: 88px;
    margin: 0 5px 5px 0;
    font-size: 12px;
    font-weight: 400;
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-decoration: none;

    &:hover {
      background: #0078d7;

      i,
      .name {
        color: #ffffff;
      }
    }

    i {
      font-size: 36px;
      margin-bottom: 10px;
      color: #0078d7;
    }

    .name {
      color: #666666;
      font-size: 13px;
    }
  }
}
</style>
