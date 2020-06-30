<template>
    <div class="about py-10">
        <v-container>
            <h2 class="about-title">نبذه عن معهد ابو قير العالي</h2>
            <p class="about-dis py-5">
                أنُشئت معاهد أبو قير العليا في عام 1998 تمشيا مع سياسة الحكومة
                المصرية لتشجيع التعليم الخاص حيث أصدر المجلس الأعلى المصري
                للجامعات والمعاهد الخاصة رخصتها والتي تعتبر صالحة اعتبارا من
                العام الدراسي 2000/2001 و تقدم مجموعة من البرامج التعليمية
                المتميزة صممت بعناية لمواكبة التغيرات و التحديات المعاصرة. فهذه
                البرامج تقوم بالتركيز على التطبيق العملي أثناء العملية التعليمية
                مما يساعد الطالب على اكتساب الأدوات اللازمة لتطوير مهاراته
                الفكرية و المعرفية و اعداده كخريجا متميزا قادرأ على مواكبة
                متطلبات سوق العمل .
            </p>
            <div class="d-flex">
                <v-btn
                    class="mx-auto white--text font-weight-bold pa-5"
                    color="bgOne"
                    >للمذيد من المعلومات</v-btn
                >
            </div>
        </v-container>
    </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.about {
    .about-title {
        position: relative;
        text-align: center;
        font-size: 2rem;
        display: block;
        width: 100%;
        font-weight: 600;
        &::before {
            position: absolute;
            content: 'About Us';
            font-size: 7rem;
            color: rgba(0, 0, 0, 0.2);
            line-height: 1;
            top: -80%;
            margin-left: -20px;
            font-weight: bold;
        }
    }
    .about-dis {
        font-weight: 600;
        text-align: center;
        line-height: 2;
        font-size: 1.5rem;
        color: #505050;
    }
}
</style>
