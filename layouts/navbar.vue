<template>
    <div>
        <v-navigation-drawer
            v-model="drawer"
            :mini-variant="miniVariant"
            :clipped="clipped"
            fixed
            app
            color="bgColor"
        >
            <v-list>
                <v-list-item>
                    <!-- <v-app-bar-nav-icon @click.stop="drawer = !drawer" /> -->
                    <v-btn icon @click.stop="miniVariant = !miniVariant">
                        <v-icon color="white"
                            >mdi-{{
                                `chevron-${miniVariant ? 'right' : 'left'}`
                            }}</v-icon
                        >
                    </v-btn>
                    <v-btn icon color="white" @click.stop="clipped = !clipped">
                        <v-icon>mdi-application</v-icon>
                    </v-btn>
                </v-list-item>

                <v-list-item
                    v-for="(item, i) in items"
                    :key="i"
                    :to="item.to"
                    router
                    exact
                    color="white"
                >
                    <v-list-item-action>
                        <v-icon>{{ item.icon }}</v-icon>
                    </v-list-item-action>
                    <v-list-item-content>
                        <v-list-item-title color="white" v-text="item.title" />
                    </v-list-item-content>
                </v-list-item>
            </v-list>
        </v-navigation-drawer>

        <!--navbar -->
        <v-app-bar
            app
            :clipped-left="clipped"
            hide-on-scroll=""
            color="bgColor"
        >
            <v-app-bar-nav-icon color="white" @click.stop="drawer = !drawer" />

            <!-- dark -->
            <v-btn icon color="white" @click="toggletheme">
                <v-icon>
                    mdi-{{
                        `${darktheme ? 'weather-night' : 'brightness-6'}`
                    }}</v-icon
                >
            </v-btn>
            <!-- Setting -->
            <v-dialog
                v-model="dialog"
                fullscreen
                hide-overlay
                transition="dialog-bottom-transition"
            >
                <template v-slot:activator="{ on, attrs }">
                    <v-btn text v-bind="attrs" v-on="on"
                        ><v-icon color="white">mdi-cog</v-icon></v-btn
                    >
                </template>
                <v-card>
                    <v-toolbar>
                        <v-toolbar-title>Settings</v-toolbar-title>
                        <v-spacer></v-spacer>
                        <v-btn @click="dialog = false"
                            ><v-icon>mdi-close</v-icon></v-btn
                        >
                    </v-toolbar>
                </v-card>
            </v-dialog>
            <v-btn>تسجيل الدخول</v-btn>

            <!-- <v-toolbar-items class="hidden-xs-only">
                <v-btn
                    v-for="item in items"
                    :key="item.id"
                    :to="item.to"
                    text
                    class="font-weight-bold"
                    nuxt
                >
                    {{ item.title }}
                </v-btn>
            </v-toolbar-items> -->
            <v-autocomplete
                v-model="select"
                :loading="loading"
                :items="itemss"
                :search-input.sync="search"
                cache-items
                class="mx-4"
                flat
                hide-no-data
                hide-details
                label="What state are you from?"
                solo-inverted
            ></v-autocomplete>
            <v-spacer />
            <img src="~/assets/logo.png" alt="" />
        </v-app-bar>
    </div>
</template>

<script>
export default {
    data() {
        return {
            dialog: false,
            darktheme: false,
            drawer: false,
            fixed: false,
            items: [
                {
                    icon: 'mdi-apps',
                    title: 'الصفحة الرئيسية',
                    to: '/',
                },
                {
                    icon: 'mdi-apps',
                    title: 'من نحن',
                    to: '/about',
                },
                {
                    icon: 'mdi-apps',
                    title: 'اتصل بنا',
                    to: '/contact',
                },
                {
                    icon: 'mdi-apps',
                    title: 'اخر الاخبار',
                    to: '/contact',
                },
                {
                    icon: 'mdi-apps',
                    title: 'نظم معلومات',
                    to: '/contact',
                },
                {
                    icon: 'mdi-apps',
                    title: 'سياحة وفنادق',
                    to: '/contact',
                },
                {
                    icon: 'mdi-apps',
                    title: 'ترميم اثار',
                    to: '/contact',
                },
            ],
            miniVariant: false,
            right: true,
            rightDrawer: false,
            title: 'معهد ابوقير العالي',
            loading: false,
            itemss: [],
            search: null,
            select: null,
            states: [
                'Alabama',
                'Alaska',
                'American Samoa',
                'Arizona',
                'Arkansas',
                'California',
                'Colorado',
                'Connecticut',
                'Delaware',
                'District of Columbia',
                'Federated States of Micronesia',
                'Florida',
            ],
        }
    },
    methods: {
        toggletheme() {
            this.$vuetify.theme.dark = !this.$vuetify.theme.dark
            this.darktheme = !this.darktheme
        },
    },
}
</script>
<style lang="scss" scoped>
.v-btn--active:hover::before,
.v-btn--active::before {
    background-color: red;
    opacity: 0.8;
}
</style>
