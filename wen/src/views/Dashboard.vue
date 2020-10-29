<template>
<v-container class="grey lighten-5">
    <v-row class="mb-6" no-gutters>
        <v-col xs="6" offset-xs="3">
            <v-card class="pa-2" outlined tile>
                .col-xs-6 .offset-xs-3
            </v-card>
        </v-col>
    </v-row>

    <v-row no-gutters>
        <v-col xs="3" offset-xs="3">
            <v-card class="pa-2" outlined tile>
                .col-xs-3 .offset-xs-3
            </v-card>
        </v-col>
        <v-col xs="3" offset-xs="3">
            <v-card class="pa-2" outlined tile>
                .col-xs-3 .offset-xs-3
            </v-card>
        </v-col>
    </v-row>
</v-container>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
    name: 'Dashboard',
    components: {}
}
</script>
