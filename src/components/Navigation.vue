<template>
    <span>
        <v-navigation-drawer app v-model="drawer" disable-resize-watcher>
            <v-list>
                <template v-for="(item, index) in items">
                    <v-list-tile :key="index">
                        <v-list-tile-content>
                            {{item.title}}
                        </v-list-tile-content>
                    </v-list-tile>
                </template>
            </v-list>
        </v-navigation-drawer>
        <v-toolbar app>
            <v-toolbar-side-icon @click="drawer = !drawer"></v-toolbar-side-icon>
        </v-toolbar>
    </span>
</template>

<script>
export default {
    name: 'AppNavigation',
    data() {
        return {
            drawer: false,
            items: [
                { title: 'Menu' },
                { title: 'Sign In' },
                { title: 'Join' }
            ]
        };
    }
};
</script>

<style>
    .theme--light
        .v-toolbar {
            background-color: transparent;
            box-shadow: none;
        }
</style>