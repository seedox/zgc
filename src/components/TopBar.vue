
<template>
<div class="header">
  <div class="top-bar">
    <div class="logo">
        <LeftMenu/>
        <span class="app-name">中关村发展集团</span>
    </div>
    <div class="search"><Input search placeholder="搜索" /></div>
    <div class="tools">
      <Notice/>
      <Settings/>
      <User/>
    </div>
  </div>
  
</div>
</template>

<script>
import LeftMenu from './LeftMenu.vue'
import Notice from './Notice.vue'
import Settings from './Settings.vue'
import User from './User.vue'
export default {
  name:"topbar",
  directives: {
  },
  components:{
    LeftMenu,
    Notice,
    Settings,
    User
  },
  data(){
    return{    
    }   
  },
 
  methods:{
    
  }
}
</script>

<style lang="scss">
.drawer{
  display:inline-block;
  width:48px;
  height:48p; 
  .icon{
    text-align: center;
    cursor:pointer;
  }
  .panel{
      display:flex;
      width:100%;
      height:60px;
      text-align: left;
      align-items: center;
      font-size: 21px;
      justify-content: space-between;
      .title{
        flex-flow: row nowrap;
        flex:1;
        font-weight: 100;
      }
      .close{
          display:flex;
          justify-content: flex-end;
          font-size: 21px;
      }
  }
  &:hover{
    background: #004578;
  }
}.active{
    background:#fff;
    color:#004578;
    &:hover{
      background: #fff;
    }
}
.top-bar{
  background: #005A9E;
  height:48px;
  line-height: 48px;
  color:#ffffff;
  display: flex;
  flex: 0 0 auto;
  .logo{
    width:220px;
    .app-name{
      margin-left:10px;
    }
    flex:0 1 auto;
  }
  .search{
    flex-grow: 1;
  }
  .tools{
    display:flex;
    flex:0 1 240px;
    justify-content: flex-end;
  }

}



</style>