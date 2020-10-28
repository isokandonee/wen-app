<template>
<nav>
    <v-app-bar flat app color="deep-purple" dark grow>
        <div id="sideicon">
            <span class="font-weight-light">Wen</span>
            <span class="font-weight-bold">App</span>
        </div>
        <v-spacer></v-spacer>
        <div id="signout" @click.stop="drawer = !drawer">
            <v-icon>mdi-menu</v-icon>
        </div>

    </v-app-bar>
    <v-navigation-drawer class="(hidden-lg-and-up: permanent=true)" dark right color="deep-purple" v-model="drawer" absolute temporary>
        <v-list-item>
            <v-list-item-avatar color="white">
                <v-img src="https://randomuser.me/api/portraits/men/78.jpg"></v-img>
            </v-list-item-avatar>
            <v-spacer></v-spacer>
            <v-list-item-content>
                <v-list-item-title>John Leider</v-list-item-title>
            </v-list-item-content>
        </v-list-item>

        <v-divider></v-divider>

        <v-list dense>
            <v-list-item v-for="item in items" :key="item.title" link>
                <v-list-item-icon>
                    <v-icon>{{ item.icon }}</v-icon>
                </v-list-item-icon>

                <v-list-item-content>
                    <v-list-item-title>{{ item.title }}</v-list-item-title>
                </v-list-item-content>
            </v-list-item>
        </v-list>
    </v-navigation-drawer>
</nav>
</template>

<script>
export default {
    name: 'Navbar',

    data: () => ({
        drawer: false,
        permanent: false,
        items: [{
                title: 'Home',
                icon: 'mdi-view-dashboard'
            },
            {
                title: 'About',
                icon: 'mdi-forum'
            },
            {
                title: 'Settings',
                icon: 'mdi-cogs'
            }, {
                title: 'Logout',
                icon: 'mdi-exit-to-app'
            }
        ],
    }),

}
</script>

<style lang="css" scoped>
#sideicon {
    cursor: pointer;
}

#signout {
    cursor: pointer;
}
</style>
