<template>
    <v-app class="home">
        <banner />
        <about />
        <sections />
    </v-app>
</template>

<script>
// import lastnews from '~/components/home/lastnews.vue'
import banner from '~/components/home/banner.vue'
import about from '~/components/home/about.vue'
import sections from '~/components/home/sections.vue'
export default {
    components: {
        banner,
        about,
        sections,
    },
}
</script>
<style lang="scss" scoped>
.home {
    height: 5000px;
}
</style>
