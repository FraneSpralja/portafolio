<template>
    <div>
        Hello from the main page!
    </div>
</template>

<script setup lang="ts">
useSeoMeta({
    title: 'Main Page',
    description: 'My Amazing Main Page',
    ogTitle: 'Main Page',
    ogDescription: 'My Amazing Main Page',
    ogImage: '[og:image]',
    ogUrl: 'localhost:3000',
    twitterTitle: 'Main Page',
    twitterDescription: 'My Amazing Main Page',
    twitterImage: '[twitter:image]',
    twitterCard: 'summary'
})
</script>