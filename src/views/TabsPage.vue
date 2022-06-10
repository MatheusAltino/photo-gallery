<template>
  <ion-page>
    <ion-tabs>
      <ion-router-outlet></ion-router-outlet>
      <ion-tab-bar slot="bottom">
        <ion-tab-button tab="tab1" href="/tabs/tab1" style="color: #fff">
          <ion-icon :icon="images" />
          <ion-label>Galeria</ion-label>
        </ion-tab-button>
        <ion-tab-button tab="tab2" href="/tabs/tab2" style="color: #fff">
          <ion-icon :icon="camera" />
          <ion-label>Photos</ion-label>
        </ion-tab-button>
        </ion-tab-bar>
    </ion-tabs>
  </ion-page>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { IonTabBar, IonTabButton, IonTabs, IonLabel, IonIcon, IonPage, IonRouterOutlet } from '@ionic/vue';
import { images, camera } from 'ionicons/icons';


export default defineComponent({
  name: 'TabsPage',
  components: { IonLabel, IonTabs, IonTabBar, IonTabButton, IonIcon, IonPage, IonRouterOutlet },
  setup() {
    return {
      images,
      camera
    }
  }
});
</script>
