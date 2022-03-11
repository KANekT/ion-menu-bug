<template>
  <ion-app>
    <keep-alive>
      <component :is="layout" />
    </keep-alive>
  </ion-app>
</template>

<script lang="ts" setup>
import { IonApp } from '@ionic/vue';
import { computed, ShallowRef } from 'vue';
import { useRoute } from 'vue-router';
import {
  AppLayoutDefault,
  AppLayoutMenu,
} from './layouts/';

const route = useRoute();

const layout: ShallowRef = computed(() => {
  switch (route.meta.layout) {
    case 'menu':
      return AppLayoutMenu;
    default:
      return AppLayoutDefault;
  }
});

</script>