<template>
  <a-layout-header :class="{ container: container }" class="app-view-header">
    <div class="app-view-header-wrapper">
      <AppLogo to="/dashboard" />
      <div class="right-section">
        <AppViewHeaderWallet />
        <AppViewHeaderUser />
      </div>
    </div>
  </a-layout-header>
</template>

<script>
export default {
  props: {
    container: {
      type: Boolean,
      default: true,
    },
  },
}
</script>

<style lang="less">
.app-view-header {
  position: absolute;
  width: 100%;
  left: 0;
  top: 0;
  height: @layout-header-height;
  background: @layout-header-background;
  box-shadow: @layout-header-shadow;
  border-top: 5px solid @primary-color;
  border-bottom: 5px solid transparent;
  box-sizing: border-box;

  &.container {
    .app-view-header-wrapper {
      position: relative;
      margin: 0 auto;
      max-width: @layout-body-container-max-width;
    }
  }

  .app-view-header-wrapper {
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .right-section {
    display: flex;
    align-items: center;
    justify-content: flex-end;
  }
}
</style>
