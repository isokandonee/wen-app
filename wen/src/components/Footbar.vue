<template>
<v-bottom-navigation class="hidden-lg-and-up" :value="value" color="deep-purple" grow>
    <v-btn to="/calculator">
        <span>Calculator</span>

        <v-icon>mdi-calculator</v-icon>
    </v-btn>

    <v-btn to="/">
        <span>Dashboard</span>

        <v-icon>mdi-home</v-icon>
    </v-btn>

    <v-btn to="/about">
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
