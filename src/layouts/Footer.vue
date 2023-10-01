<script setup></script>

<template>
    <footer class="bg-kuning text-biru-tua py-10">
        <div class="container mx-auto px-20">
            <div class="grid md:grid-cols-2">
                <div class="flex flex-col md:flex-row md:space-x-12 items-center">
                    <div class="mb-10 md:mb-0">
                        <img src="/logo.png" class="w-2/3" alt="Logo" />
                    </div>
                    <ul class="flex flex-col md:flex-row space-y-5 md:space-y-0 md:space-x-8 text-xs text-center md:text-left font-theme-heading">
                        <li class="uppercase text-[16px] font-bold hover:text-white transition duration-200">
                            <a href="#team" v-smooth-scroll>Our Team</a>
                        </li>
                        <li class="uppercase text-[16px] font-bold hover:text-white transition duration-200">
                            <a href="#portfolio" v-smooth-scroll>Our Portfolio</a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>
