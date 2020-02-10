<template>
  <ion-menu side="start" menuId="left" contentId="menu-content" type="push">
    <ion-header>
      <ion-toolbar>
        <ion-title>Left Menu</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content>
      <ion-list>
        <ion-list-header>Navigate</ion-list-header>
        <ion-menu-toggle auto-hide="false" v-for="p in appPages" :key="p.title">
          <ion-item button @click="navigate(p.url)">
            <ion-icon slot="start" :name="p.icon"></ion-icon>
            <ion-label>{{p.title}}</ion-label>
          </ion-item>
        </ion-menu-toggle>
      </ion-list>
    </ion-content>
  </ion-menu>
</template>

<script>
export default {
  name: "LeftMenu",
  data () {
    return {
      appPages: [
        {
          title: 'Home',
          url: '/',
          name: 'Home',
          icon: 'calendar'
        },
        {
          title: 'Create',
          url: '/create',
          icon: 'contacts'
        }
      ]
    }
  },
  methods: {
    navigate (url) {
      this.$router.push(url, () => { })
    }
  }
};
</script>