<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-buttons slot="start">
          <ion-menu-button menu="start"></ion-menu-button>
          <!-- <ion-menu-button menu="end"></ion-menu-button> -->
        </ion-buttons>
        <ion-title>My First App - Awesome!</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content class="ion-padding">
      <h1>Welcome To @ionic/vue</h1>
      <img alt="Vue logo" src="../assets/logo.png" />
      <br />
      <ion-button @click="$router.push({ name: 'create' })">Create</ion-button>
      <ion-button @click="presentActionSheet">Show Action Sheet</ion-button>
    </ion-content>
  </ion-page>
</template>

<script>
import { arrowDroprightCircle } from "ionicons/icons";

export default {
  name: "home",
  methods: {
    presentActionSheet () {
      return this.$ionic.actionSheetController
        .create({
          header: 'Albums',
          buttons: [
            {
              text: 'Delete',
              role: 'destructive',
              icon: 'trash',
              handler: () => {
                // eslint-disable-next-line no-console
                console.log('Delete clicked')
              },
            },
            {
              text: 'Share',
              icon: 'share',
              handler: () => {
                // eslint-disable-next-line no-console
                console.log('Share clicked')
              },
            },
            {
              text: 'Play (open modal)',
              icon: arrowDroprightCircle,
              handler: () => {
                // eslint-disable-next-line no-console
                console.log('Play clicked')
              },
            },
            {
              text: 'Favorite',
              icon: 'heart',
              handler: () => {
                // eslint-disable-next-line no-console
                console.log('Favorite clicked')
              },
            },
            {
              text: 'Cancel',
              icon: 'close',
              role: 'cancel',
              handler: () => {
                // eslint-disable-next-line no-console
                console.log('Cancel clicked')
              },
            },
          ],
        })
        .then(a => a.present())
    }
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.ion-page {
  text-align: center;
}
.pointer:hover {
  cursor: pointer;
}
</style>