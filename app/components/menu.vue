<template>
    <nav class="font-mono">
        <ul class="flex space-x-4">
            <li class="menu-link">
                <NuxtLink to="/">Main</NuxtLink>
            </li>
            <li class="menu-link">
                <NuxtLink to="/about">About</NuxtLink>
            </li>
        </ul>
    </nav>
</template>

<style scoped>
.menu-link {
    @apply p-1 hover:bg-gray-200;
}
</style>