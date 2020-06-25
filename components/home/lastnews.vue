<template>
    <div class="lastnews">
        <v-row>
            <v-col cols="8" md="10" class="pa-0"
                ><marquee behavior="scroll" direction="left" class="py-2"
                    >Lorem, ipsum dolor sit amet consectetur adipisicing elit.
                    Quisquam minus error blanditiis molestiae numquam quidem
                    similique molliti alias!</marquee
                ></v-col
            >
            <v-col cols="4" md="2" class="pa-0 py-1"
                ><h3>: اخر الاخبار</h3>
            </v-col>
        </v-row>
    </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.lastnews {
    background-color: #44bd32;
    color: white;
    height: 40px;
    width: 100%;
    text-align: center;
    overflow: hidden;
}
</style>
