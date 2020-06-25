<template>
    <v-app>
        <lastnews />

        <div class="home">
            <h2>Home</h2>
        </div>
    </v-app>
</template>

<script>
import lastnews from '~/components/home/lastnews.vue'
export default {
    components: {
        lastnews,
    },
}
</script>
<style lang="scss">
.home {
    height: 5000px;
    h2 {
        color: $color-one;
    }
}
</style>
