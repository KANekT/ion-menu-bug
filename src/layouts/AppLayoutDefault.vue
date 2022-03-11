<template>
  <transition name="slide" mode="out-in" :appear="useAppear">
    <ion-router-outlet id="main-content"></ion-router-outlet>
  </transition>
</template>

<script lang="ts" setup>
import { IonRouterOutlet } from '@ionic/vue';
import { computed, ComputedRef } from 'vue';
import { useRoute } from 'vue-router';

const route = useRoute();
const useAppear: ComputedRef<boolean> = computed(
  () => route.matched.length === 1
);
</script>

<style scoped></style>
