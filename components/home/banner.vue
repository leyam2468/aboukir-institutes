<template>
    <div class="banner">
        <v-carousel
            cycle
            show-arrows-on-hover=""
            delimiter-icon="mdi-minus"
            hide-delimiter-background
            height="calc(100vh - 50px"
        >
            <!-- Last news -->
            <lastnews />
            <!-- slider -->
            <v-carousel-item
                v-for="(item, i) in items"
                :key="i"
                :src="item.src"
            >
                <v-sheet height="100%" tile color="$overlay">
                    <v-row class="fill-height" align="center" justify="center">
                        <div class="text-center banner-title pa-5">
                            <h4 v-if="item.h4">{{ item.h4 }}</h4>
                            <h1 v-if="item.h1">{{ item.h1 }}</h1>
                            <h2 v-if="item.h2">{{ item.h2 }}</h2>
                        </div>
                    </v-row>
                </v-sheet>
            </v-carousel-item>
            <!-- Shape -->
            <div class="shape">
                <svg
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 2600 131.1"
                    preserveAspectRatio="none"
                >
                    <path
                        class="shape-fill"
                        d="M0 0L2600 0 2600 69.1 0 0z"
                    ></path>
                    <path
                        class="shape-fill"
                        style="opacity: 0.5;"
                        d="M0 0L2600 0 2600 69.1 0 69.1z"
                    ></path>
                    <path
                        class="shape-fill"
                        style="opacity: 0.25;"
                        d="M2600 0L0 0 0 130.1 2600 69.1z"
                    ></path>
                </svg>
            </div>
        </v-carousel>
    </div>
</template>

<script>
import lastnews from '@/components/home/lastnews.vue'
export default {
    components: {
        lastnews,
    },
    data() {
        return {
            items: [
                {
                    src: require('~/assets/images/banner.jpg'),
                    h4: 'مرحبا بكم في',
                    h1: 'Aboukir High Institute',
                    h2: 'معهد ابو قير العالي',
                },
                {
                    src: require('~/assets/images/b2.jpg'),
                    h4: 'المعهد العالي للحاسب الآلي ونظم المعلومات',
                },
                {
                    src: require('~/assets/images/b1.jpg'),
                    h4: 'المعهد العالي للسياحة والفنادق',
                },
                {
                    src: require('~/assets/images/b3.jpg'),
                    h4: 'المعهد العالي لترميم الاثار',
                },
            ],
        }
    },
}
</script>
<style lang="scss" scoped>
.banner {
    position: relative;
    //color: rgb(0, 0, 0, 0.8);
    .theme--dark.v-sheet {
        background-color: rgb(0, 0, 0, 0.3);
    }
    .banner-title {
        background-color: rgb(0, 0, 0, 0.3);
        h4 {
            font-size: 3rem;
        }
        h1 {
            font-size: 4rem;
        }
        h2 {
            font-size: 3rem;
        }
    }
    .shape {
        overflow: hidden;
        position: absolute;
        width: 100%;
        bottom: -1px;
        left: 0;
        transform: rotate(180deg);
        color: white;
    }
}
.v-btn--outlined .v-btn__content .v-icon,
.v-btn--round .v-btn__content .v-icon {
    color: green;
}
</style>
