<script setup>
const props = defineProps({
    btnType: String,
    link: String,
    class: {
        type: String,
        default: "text-sm sm:text-md md:text-base"
    }
});
</script>

<template>
    <a v-if="btnType === 'primary'" :href="link" v-smooth-scroll :class="class" class="font-theme-heading font-medium bg-biru-tua px-6 py-2 text-white rounded-full shadow-md hover:bg-white border-2 border-transparent hover:border-biru-tua hover:text-biru-tua cursor-pointer transition duration-200 mr-5">
        <slot></slot>
    </a>
    <a v-if="btnType === 'secondary'" :href="link" v-smooth-scroll :class="class" class="font-theme-heading font-medium bg-biru-muda px-6 py-2 text-white rounded-full shadow-md hover:bg-white border-2 border-transparent hover:border-biru-muda hover:text-biru-muda cursor-pointer transition duration-200">
        <slot></slot>
    </a>
</template>
