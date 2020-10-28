<template>
<v-app>
    <Navbar />
    <v-main>
        <router-view></router-view>
    </v-main>
    <Footbar />
</v-app>
</template>

<script>
import Navbar from '@/components/Navbar';
import Footbar from '@/components/Footbar';
export default {
    name: 'App',

    components: {
        Navbar,
        Footbar
    },

    data: () => ({
        //
    }),
};
</script>

<style scoped>
#app {
    text-align: center;
}
</style>
