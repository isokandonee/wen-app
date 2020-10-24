<template>
<v-app>
    <v-app-bar app color="deep-purple" dark>
        <div class="d-flex align-center">
            <span>Wen</span>
            <span>App</span>
        </div>
        <v-spacer></v-spacer>
        <span class="mr-2">Welcome</span>
    </v-app-bar>

    <v-main class="deep-purple lighten-5">
        <router-view></router-view>
    </v-main>
</v-app>
</template>

<script>
export default {
    name: 'App',

    components: {},

    data: () => ({
        //
    }),
};
</script>
