<template>
<div class="items">
    <div class="item">
        <div class="avatar"><Avatar icon="ios-person" size="small" /></div>
        <div class="content">
            <div class="from">信息中心-沈小会</div>
            <div class="title">欢迎使用你的新 Outlook.com 帐户</div>
            <div class="describe">晓辉 你好， 欢迎使用新的 Outlook.com 帐户。通过 Outlook 可保持联系、井井有条和高效工作 - 无论在工</div>
        </div>
        
    </div>
</div>
    
</template>

<script>
export default {
    data(){
        return {
            items:[0,1]
        }
    }
}
</script>

<style lang="scss" scoped>
.items{
    width:100%;
    .item{
        display:flex;
        width:100%;
        border-left-width: 4px;
        border-left-style: solid;
        border-left-color: transparent;
        padding-right: 24px;
        border-bottom:1px solid #eaeaea;
        padding:20px 0;
        .avatar{
            flex:0 0 auto;
            width:48px;
            text-align: center;
            padding-top:5px;
            color:#0078d7;
        }
        .content{
            display: flex;
            flex-flow: column nowrap;
            flex: 1 1 auto;
            overflow: hidden;
            user-select:none;
            .title{
                font-weight: 600;
            }
            .describe{
                white-space: nowrap;
                overflow: hidden;
                text-overflow: ellipsis;
                color:#666666;
            }
        }
        &:hover{
            background: #eaeaea;
        }
        
    }
}


</style>
