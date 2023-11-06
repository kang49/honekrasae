<template>
    <div class="bg-black min-h-max w-full px-2transition-all duration-500 px-2"
        :class="{ 'h-[15rem]': isToggleMenu, 'h-[1rem]': !isToggleMenu }">
        <div class="flex justify-between">
            <div>
                <img class="w-[3.5rem]" src="/img/honkasae_logo.png" alt="Logo" />
            </div>
            <div class="mt-2">
                <!-- Hamburger mobile menu -->
                <NuxtLink class="lg:hidden grid gap-1 mt-1 bg-black/10 p-2 rounded-md" @click="toggleMenu">
                    <span v-bind:class="{ 'rotate-45': isToggleMenu, 'translate-y-[9px]': isToggleMenu }" id="ham1"
                        class="w-6 h-1 bg-white transition-all duration-200"></span>
                    <span v-bind:class="{ 'opacity-0': isToggleMenu }" id="ham2"
                        class="w-6 h-1 bg-white transition-all duration-200"></span>
                    <span v-bind:class="{ '-rotate-45': isToggleMenu, '-translate-y-[7px]': isToggleMenu }" id="ham3"
                        class="w-6 h-1 bg-white transition-all duration-200"></span>
                </NuxtLink>
            </div>
        </div>

        <center>
            <div class="text-white mt-5 space-y-3">
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
        };
    },
    methods: {
        toggleMenu() {
            this.isToggleMenu = !this.isToggleMenu;
        },
    },
};
</script>