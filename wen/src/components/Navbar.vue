<template>
<nav>
    <v-app-bar flat app class="deep-purple" dark>
        <div id="sideicon">
            <span class="font-weight-light">Wen</span>
            <span class="font-weight-bold">App</span>
        </div>
        <v-spacer></v-spacer>
        <div id="signout" @click.stop="drawer = !drawer">
            <v-icon>mdi-menu</v-icon>
        </div>

    </v-app-bar>
    <v-navigation-drawer dark right color="deep-purple" v-model="drawer" absolute temporary>
        <v-list-item>
            <v-list-item-avatar color="white">
                <v-img src="https://randomuser.me/api/portraits/men/78.jpg"></v-img>
            </v-list-item-avatar>
            <v-spacer></v-spacer>
            <v-list-item-content @click.stop="drawer = !drawer">
                <v-list-item-title>John Leider</v-list-item-title>
            </v-list-item-content>
        </v-list-item>

        <v-divider></v-divider>

        <v-list>
            <v-list-item router :to="item.route" v-for="item in items" :key="item.title" link>
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
        // drawer: null,
        items: [{
                title: 'Home',
                icon: 'mdi-view-dashboard',
                route: '/'
            },
            {
                title: 'Blog',
                icon: 'mdi-newspaper',
                route: '/blog'
            },
            {
                title: 'Calculator',
                icon: 'mdi-calculator',
                route: '/calculator'
            },
            {
                title: 'Logout',
                icon: 'mdi-exit-to-app',
                route: '/logout'
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
