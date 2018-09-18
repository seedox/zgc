<template>
<div class="drawer" v-bind:class="{ active: showSetting }" v-click-outside="aaa" v-on:click="showSetting=true">
  <div class="icon">
    <Icon type="ios-settings" size="18" />
  </div>
  <transition name="custom-classes-transition" enter-active-class="animated slideInRight faster">
    <div class="settings" v-show="showSetting">
      <div class="panel">
        <span class="title">快速设置</span>
        <Button class="close" type="text" icon="ios-close"></Button>
      </div>
    </div>
  </transition>
</div>
</template>

<script>
import ClickOutside from "../directives/clickoutside";
export default {
  name: "setting",
  data() {
    return {
      showSetting: false
    };
  },
  directives: {
    ClickOutside
  },
  methods: {
    aaa() {
      this.showSetting = false;
    }
  }
};
</script>

<style lang="scss" scoped>
.settings {
  background: #fff;
  position: absolute;
  display: block;
  top: 48px;
  right: 0;
  bottom: 0;
  width: 279px;
  box-shadow: rgba(0, 0, 0, 0.2) -30px 0px 30px -30px;
  padding: 23px 18px 0 23px;
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-start;
  align-content: flex-start;
}
</style>
