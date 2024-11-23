<template>
    <div id="map" class="w-full h-[500px]"></div>
</template>

<script setup lang="ts">
import L from 'leaflet';
import { onMounted } from 'vue';

onMounted(() => {
    // Créer une carte et définir le centre et le niveau de zoom
    const map = L.map('map').setView([48.8566, 2.3522], 13); // Paris par défaut

    // Ajouter les tuiles OpenStreetMap
    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
        maxZoom: 19,
        // attribution:
        //     '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors',
    }).addTo(map);

    // Ajouter un marqueur
    L.marker([48.8566, 2.3522]).addTo(map).bindPopup('Bienvenue à Paris !').openPopup();
});
</script>

<style scoped>
#map {
    height: 70%;
    /* S'assure que la carte occupe tout l'espace défini */
}
</style>