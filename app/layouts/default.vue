import { NuxtLink } from '../../.nuxt/components';
<template>
    <div class="container mx-auto max-w-2xl">
        <header class="flex align-middle justify-between mt-5">
            <div>
                <NuxtLink to="/" class="text-xl font-semibold p-2 hover:bg-gray-200">Frane Spralja</NuxtLink>
            </div>
            <Menu />
        </header>
        <main class="p-2">
            <slot />
        </main>
    </div>
</template>

<script setup>

useHead({
    titleTemplate: '%s - Frane Spralja',
    link: [
        {
            rel: 'preconnect',
            href: 'https://fonts.googleapis.com',
        },
        {
            rel: 'stylesheet',
            href: 'https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap',
            crossorigin: '',
        }
    ],
})

</script>

<style>
body {
    font-family: 'Roboto';
}
</style>