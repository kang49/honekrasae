<template>
    <div class="bg-black min-h-max w-full fixed px-2 transition-all duration-500"
        :class="{ 'h-[15rem]': isToggleMenu, 'h-[4rem]': !isToggleMenu }">
        <div class="flex justify-between">
            <div>
                <img class="w-[3.5rem]" src="/img/honkasae_logo.png" alt="Logo" />
            </div>

            <div class="mt-2 lg:flex">
                <!-- Hamburger mobile menu -->
                <NuxtLink class="lg:hidden grid gap-1 mt-1 bg-black/10 p-2 rounded-md" @click="toggleMenu">
                    <span v-bind:class="{ 'rotate-45': isToggleMenu, 'translate-y-[9px]': isToggleMenu }" id="ham1"
                        class="w-6 h-1 bg-white transition-all duration-200"></span>
                    <span v-bind:class="{ 'opacity-0': isToggleMenu }" id="ham2"
                        class="w-6 h-1 bg-white transition-all duration-200"></span>
                    <span v-bind:class="{ '-rotate-45': isToggleMenu, '-translate-y-[7px]': isToggleMenu }" id="ham3"
                        class="w-6 h-1 bg-white transition-all duration-200"></span>
                </NuxtLink>

                <!--Menu Desktop-->
                <div class="space-x-2 text-white text-[16px] font-bold hidden lg:flex lg:items-center">
                    <button @click="atPages1" class="bg-black px-3 py-1 rounded-[20px]" :class="{'bg-white/50': atPages == 1}">ไม่มีอะไรแล้ว</button>
                    <button @click="atPages2" class="bg-black px-3 py-1 rounded-[20px]" :class="{'bg-white/50': atPages == 2}">มันมีแค่ข่าวเดียวอะ</button>
                    <button @click="atPages3" class="bg-black px-3 py-1 rounded-[20px]" :class="{'bg-white/50': atPages == 3}">ขี้เกียจทำต่อ</button>
                    <button @click="atPages4" class="bg-black px-3 py-1 rounded-[20px]" :class="{'bg-white/50': atPages == 4}">พอแค่นี้แหละ</button>
                </div>
            </div>
        </div>

        <center>
            <!--Set h and Condition for make menu details smooth when show-->
            <div class="text-white mt-5 space-y-3 overflow-hidden transition-all duration-[1000ms] h-0" :class="{'h-[200px]': isToggleMenu}">
                <h4 v-if="isToggleMenu">ไม่มีอะไรแล้ว</h4>
                <h4 v-if="isToggleMenu">มันมีแค่ข่าวเดียวอะ</h4>
                <h4 v-if="isToggleMenu">ขี้เกียจทำต่อ</h4>
                <h4 v-if="isToggleMenu">พอแค่นี้แหละ</h4>
            </div>
        </center>
    </div>
</template>
  
<script>
export default {
    data() {
        return {
            isToggleMenu: false,
            atPages: 1,
        };
    },
    methods: {
        toggleMenu() {
            this.isToggleMenu = !this.isToggleMenu;
        },
        atPages1() {
            this.atPages = 1;
        },
        atPages2() {
            this.atPages = 2;
        },
        atPages3() {
            this.atPages = 3;
        },
        atPages4() {
            this.atPages = 4;
        }
    },
};
</script>