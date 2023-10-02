<script setup>

import { ref } from 'vue';
import Portfolio from '../data/PortfolioData';

let isOpen = ref(1);

</script>

<template>
    <div id="portfolio" class="container mx-auto px-20 2xl:container bg-ijo pt-2 pb-20 bg-contain bg-no-repeat justify-center bg-[url('/our-Portfolio.png')]">
        <section class="py-16 mt-16">
            <div class="w-4/5 md:w-3/5 mx-auto">
                <h2 class="text-3xl text-white md:text-4xl font-semibold font-theme-heading text-center">OUR Portfolio</h2>
            </div>

            <div class="mt-10">
                <ul class="flex flex-col items-center md:flex-row justify-center font-theme-heading">
                    <li v-for="Portfolios in Portfolio" :key="Portfolios.id" :class="isOpen === Portfolios.id ? 'md:border-b-4 md:border-kuning' : ''" class="w-full md:w-56 cursor-pointer hover:text-kuning transition duration-200 border-b-2 border-t-2 md:border-t-0 flex justify-center text-white">
                        <a @click.prevent="isOpen = Portfolios.id" href="#" :class="isOpen === Portfolios.id ? 'text-kuning' : ''" class="py-5  md:border-b-0 border-b-4">{{ Portfolios.name }}</a>
                    </li>
                </ul>
            </div>

            <div class="mt-16">
                <template v-for="Portfolios in Portfolio" :key="Portfolios.id">
                    <div v-show="isOpen === Portfolios.id" class="grid gap-32 lg:grid-cols-2 items-center">
                        <div class="relative">
                            <img class="z-10 w-full" :src="Portfolios.details.imageUrl" />
                        </div>
                        <div>
                            <h3 class="text-[14px] text-2xl md:text-3xl font-medium text-center text-kuning lg:text-left">{{ Portfolios.details.title }}</h3>
                            <p class="mt-7 font-theme-content text-lg text-white text-center lg:text-left">{{ Portfolios.details.description }}</p>
                            <div class="flex justify-center lg:justify-start mt-7">
                                <LinkButton btn-type="primary" :link="Portfolios.details.link">Let&apos;s Connect</LinkButton>
                            </div>
                        </div>
                    </div>
                </template>
            </div>
        </section>
    </div>
</template>
