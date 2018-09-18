<template>
<div class="main">
    <div class="main-top"></div>
    <div class="main-container">
            <div slot="left" class="split-pane-left">
                <WorkFlow/>              
            </div>
            <div slot="right" class="split-pane-right">
                
            </div>
    </div>
</div>
    
</template>

<script>
import WorkFlow from './WorkFlow.vue'
export default {
    data () {
        return {
            split1: 0.4
        }
    },
    components:{
        WorkFlow
    }
}
</script>
<style lang="scss" scoped>
.main{
    display:flex;
    flex-grow:1;
    flex-direction: column;
    height:100%;
}
.main-top{
    background: #f4f4f4;
    width:100%;
    height:40px;
    display:flex;
    flex:0 0 auto;
    align-items:center;
}
.main-container{
    display:flex;
    flex:1 1 auto;
    border-top:1px solid #eaeaea;

}
.split-pane-left{
    width:400px;
    flex:0 0 auto;
    border-right:1px solid #eaeaea;

}

</style>