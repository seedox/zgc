<template>
<div class="aside">
  <div class="aside-top">
    <Icon class="icon" type="ios-menu" size="18" />
    <a href="/">回集团门户</a>
  </div>
  <div class="aside-container">
    <div class="collapse">
      <div class="title">
        <Icon class="icon" type="ios-arrow-down" /><span class="title-name">工作</span>
      </div>
      <div class="content">
        <div class="item active">
          <Icon class="icon" type="ios-browsers-outline" /><span>待办</span>
        </div>
        <div class="item">
          <Icon class="icon" type="ios-checkbox-outline" /><span>已办</span>
        </div>
        <div class="item">
          <Icon class="icon" type="ios-move" /><span>在办</span>
        </div>
        <div class="item">
          <Icon class="icon" type="ios-bookmarks-outline" /><span>草稿</span>
        </div>
        <div class="item">
          <Icon class="icon" type="ios-archive-outline" /><span>存档</span>
        </div>
      </div>
    </div>
    <div class="collapse">
      <div class="title">
        <Icon class="icon" type="ios-arrow-down" /><span class="title-name">云盘</span>
      </div>
      <div class="content">
        <div class="item">
          <Icon class="icon" type="ios-document-outline" /><span>文档</span>
        </div>
        <div class="item">
          <Icon class="icon" type="ios-aperture-outline" /><span>图片</span>
        </div>
        <div class="item">
          <Icon class="icon" type="ios-videocam-outline" /><span>视频</span>
        </div>
      </div>
    </div>
    <div class="collapse">
      <div class="item">
        <Icon class="icon" type="" /><a href="javascript:;">新文件夹</a>
      </div>
    </div>
  </div>
  <div class="aside-bottom">
    <Icon type="ios-mail-outline" class="icon" />
    <Icon type="ios-calendar-outline" class="icon" />
    <Icon type="ios-contacts-outline" class="icon" />
    <Icon type="ios-more" class="icon" />
  </div>
</div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.aside {
  background: #f4f4f4;
  display: flex;
  width: 220px;
  flex: 0 0 auto;
  flex-direction: column;
}

.aside-top {
  display: flex;
  align-items: center;
  height: 40px;
  flex: 0 0 auto;

  .icon {
    width: 48px;
    height: 40px;
    line-height: 40px;
    text-align: center;
    cursor: pointer;
  }
}

.aside-container {
  flex: 1 1 auto;
  border: 1px solid #eaeaea;

  .collapse {
    font-size: 14px;

    .title {
      font-weight: 700;
      cursor: pointer;
      height: 48px;
      line-height: 48px;
    }

    .icon {
      width: 1em;
      margin: 0 16px;
    }

    .content {
      .item {
        height: 36px;
        line-height: 36px;
        cursor: pointer;

        &:hover {
          background: #eaeaea;
        }
      }

      .active {
        background: #c7e0f4;
        color: #0078d7;
        font-weight: 700;
      }
    }
  }
}

.aside-bottom {
  display: flex;
  flex: 0 0 auto;
  align-items: center;
  height: 40px;
  justify-content: space-around;

  .icon {
    font-size: 18px;
  }

  width: 100%;
}
</style>
