<template>
    <ion-page>
        <ion-header>
            <ion-toolbar>
                <ion-title>Photo Gallery</ion-title>
            </ion-toolbar>
        </ion-header>
        <ion-content :fullscreen="true">
            <ion-header collapse="condense">
                <ion-toolbar>
                    <ion-title size="large">Tab 2</ion-title>
                </ion-toolbar>
            </ion-header>

            <ion-fab vertical="bottom" horizontal="center" slot="fixed">
                <ion-fab-button @click="takePhoto()">
                    <ion-icon :icon="camera"/>
                </ion-fab-button>
            </ion-fab>

        </ion-content>
    </ion-page>
</template>


<script setup lang="ts">

import {IonPage, IonHeader, IonToolbar, IonTitle, IonContent} from '@ionic/vue';
import {camera} from "ionicons/icons";
import {usePhotoGallery} from "@/composables/usePhotoGallery";

const {takePhoto} = usePhotoGallery();
</script>


