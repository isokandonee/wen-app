<template>
<v-bottom-navigation :value="value" color="deep-purple" grow>
    <v-btn>
        <span>Recents</span>

        <v-icon>mdi-history</v-icon>
    </v-btn>

    <v-btn>
        <span>Home</span>

        <v-icon>mdi-home</v-icon>
    </v-btn>

    <v-btn>
        <span>Nearby</span>

        <v-icon>mdi-map-marker</v-icon>
    </v-btn>
</v-bottom-navigation>
</template>

<script>
export default {
    name: 'Footbar',
    data: () => ({
        value: 1
    }),
}
</script>
