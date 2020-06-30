<template>
    <div class="lastnews">
        <v-row>
            <v-col cols="8" md="10" class="pa-0"
                ><marquee behavior="scroll" direction="left"
                    ><v-btn text class="font-weight-bold"
                        >تنبية هآم لطلاب الفرقة الرابعة بالمعهد العالي للسياحة
                        والفنادق تم تعديل مواعيد جدول امتحانات الفصل الدراسي
                        الثاني طبقا لتعليمات وزارة التعليم العالي والمجلس الأعلي
                        للجامعات بشأن عدم تعارضها مع إمتحانات الثانوية
                        العامة</v-btn
                    >
                </marquee></v-col
            >
            <v-col cols="4" md="2" class="pa-0 py-1"
                ><h3>: اخر الاخبار</h3>
            </v-col>
        </v-row>
    </div>
</template>

<script>
export default {
    data() {
        return {}
    },
}
</script>

<style lang="scss" scoped>
.lastnews {
    background-color: rgba(0, 0, 0, 0.5);
    color: white;
    height: 40px;
    width: 100%;
    text-align: center;
    overflow: hidden;
    position: absolute;
    top: 0;
    z-index: 2;
}
</style>
