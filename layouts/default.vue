<template>
    <v-app>
        <navbar />
        <v-main>
            <nuxt />
        </v-main>
    </v-app>
</template>

<script>
import navbar from '~/layouts/navbar.vue'
export default {
    components: {
        navbar,
    },
}
</script>

<style lang="scss">
a {
    text-decoration: none;
}
</style>
