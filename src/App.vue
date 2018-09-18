<template>
<div id="app">
  <TopBar />
  <div class="container">
    <Aside />
    <Main />
  </div>
</div>
</template>

<script>
import TopBar from "./components/TopBar.vue";
import Aside from "./components/Aside.vue";
import Main from "./components/Main.vue";

export default {
  name: "app",
  components: {
    TopBar,
    Aside,
    Main
  }
};
</script>

<style lang="scss">
html,
body {
  height: 100%;
}

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  height: 100%;
  display: flex;
  flex-direction: column;
  user-select: none;
}

.container {
  display: flex;
  flex: 1;
}

.items {
  width: 100%;

  .item {
    display: flex;
    width: 100%;
    border-left-width: 4px;
    border-left-style: solid;
    border-left-color: transparent;
    padding-right: 24px;
    border-bottom: 1px solid #eaeaea;
    padding: 20px 0;

    .avatar {
      flex: 0 0 auto;
      width: 48px;
      text-align: center;
      padding-top: 5px;
      color: #0078d7;
    }

    .content {
      display: flex;
      flex-flow: column nowrap;
      flex: 1 1 auto;
      overflow: hidden;
      user-select: none;

      .title {
        font-weight: 600;
      }

      .describe {
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;
        color: #666666;
      }
    }

    &:hover {
      background: #eaeaea;
    }
  }
}
</style>
