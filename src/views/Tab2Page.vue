<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Tire uma Superfoto</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-fab vertical="bottom" horizontal="center" slot="fixed">
        <ion-fab-button @click="takePhoto()">
          <ion-icon :icon="camera"></ion-icon>
        </ion-fab-button>
      </ion-fab>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { camera, trash, close } from 'ionicons/icons'
import { usePhotoGallery, UserPhoto } from '@/composables/usePhotoGallery';
import { IonPage, IonHeader, IonFab, IonFabButton, IonIcon, IonToolbar, IonTitle, IonContent } from '@ionic/vue';
import { useRoute } from 'vue-router';

export default defineComponent({
  name: 'Tab2Page',
  components: {
    IonPage,
    IonHeader,
    IonFab,
    IonFabButton,
    IonIcon,
    IonToolbar,
    IonTitle,
    IonContent,
  },
  setup() {
    const { takePhoto } = usePhotoGallery();
    return {
      takePhoto,
      camera,
      trash,
      close
    }
  }
});
</script>

<style>

</style>