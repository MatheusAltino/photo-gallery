<template>
    <ion-page>
      <ion-grid>
        <ion-row>
          <ion-col size="6" :key="photo" v-for="photo in photos">
            <ion-img :src="photo.webviewPath"></ion-img>
          </ion-col>
        </ion-row>
      </ion-grid>
    </ion-page>
</template>

<script lang="ts">
import { usePhotoGallery, UserPhoto } from '@/composables/usePhotoGallery';
import { defineComponent } from 'vue';
import { IonPage, IonGrid, IonRow, IonCol, IonImg } from '@ionic/vue';


export default defineComponent({
  props: ['photos'],
  name: 'PhotosList',
  components: {
    IonPage,
    IonGrid,
    IonRow,
    IonCol,
    IonImg
  },
  setup() {
      const { photos } = usePhotoGallery();
      return {
        photos
      }
  }
})
</script>