<template>
    <div class="sections">
        <v-container>
            <h2 class="sections-title">اقسام المعهد</h2>
            <!-- one -->
            <v-row class="py-10">
                <v-col md="6">
                    <div>
                        <h2 class="pb-8">
                            المعهد العالي للحاسب الآلي ونظم المعلومات
                        </h2>
                        <p class="sections-prag">
                            يمنح درجة البكالوريوس في نظم المعلومات الإدارية
                            بقرار الانشاء رقم 1434 في 10/9/200 وقرار المعادلة
                            الصادر من المجلس الأعلي للجامعات رقم 244 في
                            22/9/2013 بمعادلة درجة البكالوريوس في شعبه نظم
                            الملومات الادارية التي يمنحها المعهد بدرجة
                            البكالوريوس في التجارة ( إدارة الاعمال - نظم
                            المعلومات الادارية ) التي تمنحها الجامعات المصرية.
                        </p>
                        <v-btn
                            class="px-8 mt-5 font-weight-black white--text"
                            large=""
                            elevation="8"
                            color="bgOne"
                            >اقراء المزيد</v-btn
                        >
                    </div>
                </v-col>
                <v-col md="6"
                    ><img
                        src="~/assets/images/b2.jpg"
                        alt=""
                        width="100%"
                        height="100%"
                        class="pa-2 elevation-10"
                /></v-col>
            </v-row>
            <!-- tow -->
            <v-row class="py-10">
                <v-col md="6"
                    ><img
                        src="~/assets/images/b1.jpg"
                        alt=""
                        width="100%"
                        height="100%"
                        class="pa-2 elevation-10"
                /></v-col>
                <v-col md="6">
                    <div class="text-right">
                        <h2 class="pb-8">
                            المعهد العالى للسياحة والفنادق
                        </h2>
                        <p class="sections-prag">
                            التخصصات:بكالوريوس دراسات سياحية شعبة ( إدارة
                            الأعمال السياحية – إدارة شراكات الطيران – إدارة
                            شركات الملاحة – إدارة الأحداث الخاصة – إدارة الأحداث
                            الرياضية)بكالوريوس إدارة الضيافة شعبة ( إدارة
                            الفنادق – إدارة المطاعم – إدارة خدمات الضيافة الجوية
                            والبحرية – إدارة فنون الطهي – إدارة خدمة العملاء –
                            إدارة الاحداث الخاصة)
                        </p>

                        <v-btn
                            class="px-8 mt-5 font-weight-black white--text"
                            large=""
                            elevation="8"
                            color="bgOne"
                            >اقراء المزيد</v-btn
                        >
                    </div>
                </v-col>
            </v-row>
            <!-- three -->
            <v-row class="py-10">
                <v-col md="6">
                    <div>
                        <h2 class="pb-8">
                            المعهد العالي لترميم الآثار
                        </h2>
                        <p class="sections-prag">
                            حيث هو معهــد ترميـــم الآثار الخاص الوحيد في
                            مصــــر يحصل الخريج علي درجة البكالوريوس في الإرشاد
                            السياحي المعادل لدرجة بكالوريوس الارشاد السياحي التي
                            تمنحة الجامعات المصرية بقرار المجلس الاعلي للجامعات
                            بالقرار الوزارى رقم 201 لسنة 2009 هو تخصص دقيق ضمن
                            تخصصات أقسام كليات الاثار فهو يهتم بدراسة مواد
                            الأثار وصيانتها سواء كانت عضوية او غير عضوية.
                        </p>
                        <v-btn
                            class="px-8 mt-5 font-weight-black white--text"
                            large=""
                            elevation="8"
                            color="bgOne"
                            >اقراء المزيد</v-btn
                        >
                    </div>
                </v-col>
                <v-col md="6"
                    ><img
                        src="~/assets/images/b3.jpg"
                        alt=""
                        width="100%"
                        height="100%"
                        class="pa-2 elevation-10"
                    />
                </v-col>
            </v-row>
        </v-container>
    </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.sections {
    .sections-title {
        position: relative;
        text-align: center;
        font-size: 2rem;
        display: block;
        width: 100%;
        font-weight: 600;
        &::before {
            position: absolute;
            content: 'Sectons';
            font-size: 3.5em;
            color: rgba(0, 0, 0, 0.2);
            line-height: 1;
            top: -80%;
            margin-left: -100px;
            font-weight: bold;
        }
    }
    .sections-prag {
        font-size: 1.5rem;
        color: #505050;
        line-height: 1.5;
    }
}
</style>
