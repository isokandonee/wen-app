<template>
<v-container fluid>
    <v-app>
        <Navbar class="hidden-md-and-down" />
        <MobileNavbar class="hidden-lg-and-up" />
        <v-main>
            <router-view></router-view>
        </v-main>
        <Footbar class="hidden-lg-and-up" />
    </v-app>
</v-container>
</template>

<script>
import Navbar from '@/components/Navbar';
import Footbar from '@/components/Footbar';
import MobileNavbar from '@/components/MobileNavbar';

export default {
    name: 'App',

    components: {
        Navbar,
        Footbar,
        MobileNavbar
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
