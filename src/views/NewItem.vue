<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-buttons slot="start">
          <ion-menu-button menu="start"></ion-menu-button>
          <!-- <ion-menu-button menu="end"></ion-menu-button> -->
        </ion-buttons>
        <ion-title></ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content padding>
      <ion-title>New Item</ion-title>
    </ion-content>
    <ion-fab vertical="bottom" horizontal="end" slot="fixed">
      <ion-fab-button @click="$router.go(-1)">
        <v-icon dark>mdi-arrow-left</v-icon>
      </ion-fab-button>
    </ion-fab>
  </ion-page>
</template>

<script>
export default {
  name: "NewItem"
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
