<template>
<div class="drawer" v-bind:class="{ active: showNotice }"
        v-click-outside="aaa" v-on:click="showNotice=true">
        <div class="icon"><Icon type="ios-notifications" size="18"/></div>
        <transition name="custom-classes-transition"
              enter-active-class="animated slideInRight faster">
            <div class="notice" v-show="showNotice">
                <div class="panel">
                    <span class="title">收到消息</span><Button class="close" type="text" icon="ios-close"></Button>
                </div>
                <div class="items">
                    <div class="item">
                        <div class="avatar"><Avatar icon="ios-person" size="small" /></div>
                        <div class="content">
                            <div class="from">信息中心-沈小会</div>
                            <div class="title">欢迎使用你的新 Outlook.com 帐户</div>
                            <div class="describe">晓辉 你好， 欢迎使用新的 Outlook.com 帐户。通过 Outlook 可保持联系、井井有条和高效工作 - 无论在工</div>
                        </div>                   
                    </div>
                    <div class="item">
                        <div class="avatar"><Avatar icon="ios-person" size="small" /></div>
                        <div class="content">
                            <div class="from">信息中心-沈小会</div>
                            <div class="title">欢迎使用你的新 Outlook.com 帐户</div>
                            <div class="describe">晓辉 你好， 欢迎使用新的 Outlook.com 帐户。通过 Outlook 可保持联系、井井有条和高效工作 - 无论在工</div>
                        </div>                   
                    </div>
                </div>
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
            showNotice:false
        }
    },
    directives:{
        ClickOutside
    },
    methods:{
        aaa(){
            this.showNotice = false;
        }
    }
}
</script>
<style lang="scss" scoped>
.notice{
  background:#fff;
  position:absolute;
  display:block;
  top:48px;
  right:0;
  bottom:0;
  width:350px;
  box-shadow: rgba(0, 0, 0, 0.2) -30px 0px 30px -30px;
  padding:23px 18px 0 23px;
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-start;
  align-content: flex-start;
}
</style>
