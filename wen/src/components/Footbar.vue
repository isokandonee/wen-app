<template>
<v-bottom-navigation :value="value" color="deep-purple" grow app>
    <v-btn to="/calculator">
        <span>Calculator</span>

        <v-icon>mdi-calculator</v-icon>
    </v-btn>

    <v-btn to="/">
        <span>Home</span>

        <v-icon>mdi-home</v-icon>
    </v-btn>

    <v-btn to="/blog">
        <span>Blog</span>

        <v-icon>mdi-newspaper</v-icon>
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
