<template>
  <div id="app">
    <ion-app>
      <ion-split-pane>
        <!-- <RightMenu /> -->
        <LeftMenu />
        <ion-vue-router main id="menu-content" />
      </ion-split-pane>
    </ion-app>
    <ion-menu-controller></ion-menu-controller>
  </div>
</template>

<script>
// import RightMenu from "./components/RightMenu.vue";
import Leftmenu from "./components/LeftMenu.vue";
export default {
  name: "app",
  components: {
    // 'RightMenu': RightMenu,
    'LeftMenu': Leftmenu
  }
}
</script>

<style>
ion-navbar.toolbar.toolbar-ios.statusbar-padding,
ion-navbar.toolbar-ios ion-title.title-ios,
ion-toolbar.toolbar.toolbar-ios.statusbar-padding,
ion-toolbar.toolbar-ios ion-title.title-ios {
  padding-top: constant(safe-area-inset-top);
  padding-top: env(safe-area-inset-top);
}
</style>