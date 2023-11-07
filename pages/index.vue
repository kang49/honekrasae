<template>
    <Navbar />
    <div class="min-h-[92vh] pt-[50px] min-w-screen">
        <div class="flex justify-center mt-[30px] space-x-5 mx-6 lg:justify-between lg:items-start">
            <img class="w-[95%] lg:w-[40rem] lg:object-contain" src="/img/poster-news.png">

            <!--More News Box Desktop-->
            <div class="bg-[#8888] min-w-[17rem] w-full max-h-[28.3rem] py-7 px-6 hidden lg:block overflow-y-auto">
                <h1 class="text-black text-[30px] font-bold">ข่าวอื่นๆ</h1>

                <div class="my-5 space-y-3">
                    <div class="min-w-full flex items-center">
                        <div class="pr-5">
                            <img class="w-[200px]" src="/img/time.png">
                        </div>
                        <div class="flex justify-end">
                            <h4 class="text-[20px] font-bold text-black max-w-[280px]">
                                หูแตก!! พรี่ไทม์ก่อเกียรติร้องคาราโอเกะดังมิดแอมป์ เพื่อนบาดเจ็บสาหัส
                            </h4>
                        </div>
                    </div>
                    <div class="min-w-full flex items-center">
                        <div class="pr-5">
                            <img class="w-[200px]" src="/img/pipe170.png">
                        </div>
                        <div class="flex justify-end">
                            <h4 class="text-[20px] font-bold text-black max-w-[280px]">
                                พัง!! ไปร์สง่ะทำจอไอโฟนน้องม.4แตก เหตุเสริฟวอลเลย์โดนหลัง สูญราว $170
                            </h4>
                        </div>
                    </div>
                    <div class="min-w-full flex items-center">
                        <div class="pr-5">
                            <img class="w-[200px]" src="/img/pipe-like.png">
                        </div>
                        <div class="flex justify-end">
                            <h4 class="text-[20px] font-bold text-black max-w-[280px]">
                                ดีใจจนยกนิ้ว!! น้องไปร์สสารวิทยาแข่ง A-Math ได้รางวัลชนะเลิศ พ่อแม่กลั้นน้ำตาไม่อยู่
                            </h4>
                        </div>
                    </div>
                </div>
            </div>

            <!--Text Size Button Desktop-->
            <div
                class="w-[3rem] h-[130px] bg-[#8888] rounded-[20px] mb-6  flex-col items-center space-y-3 px-2 justify-center hidden lg:flex">
                <div class="text-[12px] flex justify-center border-b border-[#000] pb-2"
                    :class="{ 'text-blue-600': textSize == 12 }">
                    <button class="fas fa-font" @click="textSize12"></button>
                </div> <!--Row1-->

                <div class="text-[16px] flex justify-center border-b border-[#000] pb-2"
                    :class="{ 'text-blue-600': textSize == 16 }">
                    <button class="fas fa-font" @click="textSize16"></button>
                </div> <!--Row2-->

                <div class="text-[25px] flex justify-center" :class="{ 'text-blue-600': textSize == 25 }">
                    <button class="fas fa-font" @click="textSize25"></button>
                </div> <!--Row3-->
            </div>
        </div>
        <!--Date-->
        <div class="flex justify-between items-center mt-5">
            <div class="ml-6 text-[#8888]">
                <h4><i class="far fa-calendar-alt mr-2"></i>7 พ.ย. 2566 16:20 น.</h4>
            </div>

            <!--Text Size Button-->
            <div
                class="h-[3rem] min-w-[150px] bg-[#8888] rounded-[20px] mr-6 grid grid-cols-3 items-center space-x-1 px-2 lg:hidden">
                <div class="text-[12px] flex justify-center border-r border-[#000] pr-2"
                    :class="{ 'text-blue-600': textSize == 12 }">
                    <button class="fas fa-font" @click="textSize12"></button>
                </div> <!--Col1-->

                <div class="text-[16px] flex justify-center border-r border-[#000] pr-2"
                    :class="{ 'text-blue-600': textSize == 16 }">
                    <button class="fas fa-font" @click="textSize16"></button>
                </div> <!--Col2-->

                <div class="text-[25px] flex justify-center" :class="{ 'text-blue-600': textSize == 25 }">
                    <button class="fas fa-font" @click="textSize25"></button>
                </div> <!--Col3-->
            </div>
        </div>

        <!--Horizon line-->
        <div class="min-w-full flex justify-center my-5">
            <div class="bg-[#8888] w-[25rem] h-[2px] lg:w-[80%]"></div>
        </div>

        <!--News body-->
        <div class="w-full flex justify-start px-6 text-[25px] font-bold mb-5">
            <h4>ระวัง!! ตกเป็นผู้ต้องหาไม่รู้ตัว จากการขายบัญชีม้าให้มิจฉาชีพ</h4>
        </div>
        <div class="min-w-full flex justify-center">
            <div class="w-[90%] h-max text-black"
                :class="{ 'text-[12px]': textSize == 12 }, { 'text-[16px]': textSize == 16 }, { 'text-[25px]': textSize == 25 }">
                <!--ส่วน1-->
                <h4><b>รู้จัก “บัญชีม้า” เครื่องมือประกอบการก่อเหตุที่สำคัญของเหล่ามิจฉาชีพ
                        แต่ขณะเดียวกันก็สามารถใช้เป็นทริคเอาตัวรอดจากการตกเป็นเหยื่อได้ พร้อมเปิดโทษหนักทั้งปรับและจำคุก
                        ใครที่คิดจะอาสารับงานนี้ คงต้องระวังให้มากๆ เรื่องนี้ต้องเตือนดังๆ ด้วยความหวังดี</b><br><br>คำนี้
                    ประโยคนี้ กลับมาสร้างกระแสความฮือฮาอีกครั้ง ด้วยสาเหตุสืบเนื่องจากวันที่ 25 กันยายน 2566 ที่ผ่านมา
                    ตำรวจไซเบอร์ นำหมายศาลไปบุกค้นบ้าน <b>“บิ๊กโจ๊ก”</b> หรือ <b>พล.ต.อ.สุรเชษฐ์ หักพาล</b>
                    รองผู้บัญชาการตำรวจแห่งชาติ (รอง ผบ.ตร.)
                    เพื่อขอตรวจค้นและจับกุมลูกน้องคนใกล้ชิดซึ่งถูกกล่าวหาเกี่ยวข้องกับ
                    “บัญชีม้า” เนื่องจากพบว่ามีเส้นทางการเงินที่เกี่ยวข้องกับ<b>เว็บไซต์พนันออนไลน์</b>
                </h4>

                <!--ส่วน2---->
                <h4 v-if="isreadmoreBTN">
                    <br>ชวนคอข่าวทำความรู้จัก <b class="text-red-600">“บัญชีม้า”</b><br><br>

                    &nbsp;&nbsp;&nbsp;&nbsp;<b>บัญชีม้า</b> คือ บัญชีที่ถูกเปิดเพื่อผลประโยชน์บางอย่าง เช่น
                    นำไปใช้ทำเรื่องผิดกฎหมาย หรือเอาไว้ใช้สำหรับถ่าย เท หรือใช้ในการฟอกเงิน
                    โดยบัญชีม้าคนที่ถือครองบัญชีมักจะไม่ใช้เจ้าของตัวจริง แต่จะเป็นของมิจฉาชีพนำไปใช้
                    ซึ่งส่วนใหญ่มิจฉาชีพจะใช้วิธีการจ้างวานคนทั่ว ๆ ไปให้ทำการเปิดบัญชีธนาคาร
                    โดยให้เงินค่าจ้างแล้วแต่ตกลงกัน ซึ่งส่วนใหญ่มิจฉาชีพมักมองหาเหยื่อที่อยู่ในช่วงวัยรุ่น หรือคนสูงอายุ
                    เพราะใช้เงินเป็นตัวหลอกล่อให้ตกหลุมพราง หรืออีกวิธีก็คือการสวมรอยเป็นเจ้าของบัญชี
                    โดยการขโมยข้อมูลส่วนตัว เช่น ชื่อ-นามสกุล เบอร์โทรศัพท์ และหมายเลขบัตรประชาชนจำนวน 13 หลัก
                    แล้วนำไปเปิดบัญชีออนไลน์ กว่าจะเจ้าของข้อมูลจะรู้ตัว ก็สายไปเสียแล้ว<br><br>

                    <p class="text-red-600">บัญชีม้า อันตรายยังไง ขนาดไหน?</p><br>&nbsp;&nbsp;&nbsp;&nbsp;
                    มิจฉาชีพส่วนใหญ่มักมีกลอุบายในการโกงและทำงานกันเป็นขบวนการ ส่วนใหญ่มิจฉาชีพมักมีบัญชีม้าหลายบัญชี
                    เพื่อใช้การโอนเงินส่งต่อกันเป็นทอดๆ จากอีกหนึ่งบัญชีสู่อีกหนึ่งบัญชี อาจมีการส่งต่อมากกว่า 4-5 บัญชี
                    เพื่อป้องกันตัวเองจากการตรวจสอบของตำรวจหรือการถูกอายัดเงิน<br><br>

                    <b>จับกลลวงมิจฉาชีพด้วยบัญชีม้า</b><br><br> &nbsp;&nbsp;&nbsp;&nbsp;
                    หลายครั้งมิจฉาชีพมักเข้ามาด้วยการแอบอ้างเป็นหน่วยงานรัฐหรือเอกชน
                    ทำให้หลายคนตกหลุมพรางแล้วตามที่มิจฉาชีพบอกด้วยความกลัวว่าจะถูกดำเนินคดีตามที่ถูกข่มขู่ อาทิ
                    การถูกสั่งให้โอนเงินมาเพื่อตรวจสอบต่างๆ มิฉะนั้นจะถูกดำเนินคดีตามกฎหมาย เป็นต้น<br><br>
                    &nbsp;&nbsp;&nbsp;&nbsp; ทั้งนี้ หากพิจารณาอย่างถี่ถ้วนแล้วจะพบว่า
                    หน่วยงานราชการและเอกชนส่วนใหญ่มักจะมีการส่งหนังสือหรือเอกสารที่เป็นลายลักษณ์อักษรมาชี้แจงด้วยเสมอ
                    หากเกิดเหตุการณ์ต้องสงสัยขึ้นกับทรัพย์สินหรือเงินของบุคคลใดก็ตาม
                    และที่สำคัญหากต้องมีการโอนเงินหรือทำธุรกรรมทางการเงินอื่นๆ บัญชีที่ใช้ก็มักเป็นบัญชีของหน่วยงาน
                    ไม่ใช่บัญชีบัญชีส่วนบุคคล<br><br>

                    &nbsp;&nbsp;&nbsp;&nbsp; ดังนั้น การจับสังเกตบัญชีม้า จึงสามารถใช้เป็นทริกในการจับกลลวงของมิจฉาชีพได้
                    เพราะถึงแม้จะมีการแอบอ้างเป็นหน่วยงานใดก็ตาม
                    บัญชีม้าที่เหล่ามิจฉาชีพใช้กันนั้นมักจะเป็นบัญชีส่วนบุคคลเสมอ
                </h4>
            </div>
        </div>
        <div class="min-w-full flex justify-center my-5">
            <button v-if="!isreadmoreBTN"
                class="w-[6rem] h-[2rem] text-[#0082F6] border-[2px] border-[#0082F6] flex justify-center items-center rounded-[20px]"
                @click="readmoreToggle">
                <h4>อ่านต่อ</h4>
            </button>
        </div>

        <!--Horizon line-->
        <div class="min-w-full flex justify-center mt-[50px] mb-[20px]">
            <div class="bg-[#8888] w-[25rem] h-[2px] lg:hidden"></div>
        </div>

        <!--More News Box Mobile-->
        <div class="bg-[#8888] min-w-full py-7 px-6 lg:hidden">
            <h1 class="text-black text-[30px] font-bold">ข่าวอื่นๆ</h1>

            <div class="my-5 space-y-3">
                <div class="min-w-full flex items-center">
                    <div class="pr-5">
                        <img class="w-[200px]" src="/img/time.png">
                    </div>
                    <div class="flex justify-end">
                        <h4 class="text-[20px] font-bold text-black max-w-[280px]">
                            หูแตก!! พรี่ไทม์ก่อเกียรติร้องคาราโอเกะดังมิดแอมป์ เพื่อนบาดเจ็บสาหัส
                        </h4>
                    </div>
                </div>
                <div class="min-w-full flex items-center">
                    <div class="pr-5">
                        <img class="w-[200px]" src="/img/pipe170.png">
                    </div>
                    <div class="flex justify-end">
                        <h4 class="text-[20px] font-bold text-black max-w-[280px]">
                            พัง!! ไปร์สง่ะทำจอไอโฟนน้องม.4แตก เหตุเสริฟวอลเลย์โดนหลัง สูญราว $170
                        </h4>
                    </div>
                </div>
                <div class="min-w-full flex items-center">
                    <div class="pr-5">
                        <img class="w-[200px]" src="/img/pipe-like.png">
                    </div>
                    <div class="flex justify-end">
                        <h4 class="text-[20px] font-bold text-black max-w-[280px]">
                            ดีใจจนยกนิ้ว!! น้องไปร์สสารวิทยาแข่ง A-Math ได้รางวัลชนะเลิศ พ่อแม่กลั้นน้ำตาไม่อยู่
                        </h4>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <Footer />
</template>

<script>
export default {
    //Set variable
    data() {
        return {
            isreadmoreBTN: false,
            textSize: 16,
        }
    },
    methods: {
        readmoreToggle() {
            this.isreadmoreBTN = true;
        },
        textSize12() {
            this.textSize = 12;
        },
        textSize16() {
            this.textSize = 16;
        },
        textSize25() {
            this.textSize = 25;
        }
    }
}
</script>