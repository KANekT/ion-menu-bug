<template>
  <ion-page>
    <ion-content class="ion-padding">
      <div class="not-found">
        <div class="not-found--block">
          <p>
          </p>
          <ion-button @click="() => router.back()">
            back
          </ion-button>
        </div>
      </div>
    </ion-content>
  </ion-page>
</template>

<script lang="ts" setup>
import { IonContent, IonPage, IonButton } from '@ionic/vue';
import { useRouter } from 'vue-router';
const router = useRouter();
console.log('setup NotFound Page');
</script>

<style>
.not-found {
  display: flex;
  width: 100%;
  height: 100%;
  align-items: center;
  justify-content: center;
}
.not-found--block {
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 100%;
  align-items: center;
  justify-content: center;
}
.not-found--block p {
  text-align: center;
  font-size: 2rem;
}
</style>
