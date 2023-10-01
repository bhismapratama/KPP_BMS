<script setup></script>

<template>
    <!-- Hero Section Start -->
    <div class="xl:container mx-auto overflow-hidden relative sm:w-full pt-44 sm:pt-20 xl:px-20 px-5 overflow-x-hidden lg:overflow-x-visible h-screen lg:h-[90vh] sm:h-full bg-kuning" id="hero">
        <section class="grid grid-cols-none lg:grid-cols-2 pb-16 pt-8 items-center">
            <div class="lg:w-5/6 order-2 lg:order-none xl:pl-10 pt-8 z-10">
                <h1 class="text-6xl xl:text-[90px] font-bold font-theme-heading text-center lg:text-left ">Welcome To Our Website</h1>
                <p class="lg:text-xl mt-10 text-[20px] text-black text-center lg:text-left">Telusuri informasi lebih lanjut tentang tim kami di sini.</p>
                <div class="flex justify-center lg:justify-start mt-10">
                    <LinkButton btn-type="primary" link="#team">Our Team</LinkButton>
                    <LinkButton btn-type="secondary" link="#portfolio">Our Portfolio</LinkButton>
                </div>
            </div>
            <div>
                <img class="w-full absolute right-[50%] bottom-0 sm:hidden lg:block lg:w-[50%] lg:right-20" src="/biru.png" />
                <img class="absolute right-[-35%] top-[-90px] w-2/3 sm:hidden lg:block lg:w-[30%] lg:right-0 lg:top-[-150px]" src="/ijo.png" />
            </div>
        </section>
    </div>
    <!-- Hero Section End -->
</template>
