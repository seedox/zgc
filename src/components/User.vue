<template>
<div class="drawer" v-bind:class="{ active: showUser }"
        v-click-outside="aaa" v-on:click="showUser=true">
        <div class="icon"><Icon type="md-person" size="20"/></div>   
        <transition name="custom-classes-transition"
              enter-active-class="animated slideInRight faster">
            <div class="user-info" v-show="showUser">
                <div class="panel">
                    <span class="title">我的账户</span><Button class="close" type="text" icon="ios-close"></Button>
                </div>
                <div class="avatar">
                    <Avatar icon="ios-person" size="large" /><span class="name">沈小辉</span>
                </div>
                <div class="item-text">信息中心副主任</div>
                <div class="item-text"><a href="javascript:;">编辑个人资料</a></div>
                <div class="item-text"><a href="javascript:;">注销</a></div>
            </div>
        </transition>
</div>   
</template>
<script>
import ClickOutside from '../directives/clickoutside'

export default {
    name:"notice",
    data(){
        return{
            showUser:false
        }
    },
    directives:{
        ClickOutside
    },
    methods:{
        aaa(){
            this.showUser = false;
        }
    }
}
</script>
<style lang="scss" scoped>
.user-info{
  background:#fff;
  position:absolute;
  top:48px;
  right:0;
  bottom:0;
  width:279px;
  line-height: 40px;
  box-shadow: rgba(0, 0, 0, 0.2) -30px 0px 30px -30px;
  padding:10px 18px 0 23px;
  .avatar{
      width:100%;
      text-align: left;
      .name{
          padding-left:16px;
      }
  }
  .item-text{
      margin-left:8px;
  }
}
</style>
