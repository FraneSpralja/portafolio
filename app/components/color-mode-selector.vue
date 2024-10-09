<template>
    <div>
        <span v-if="showLabel" class="text-gray-500 pe-2">Change to: {{ nextMode }}</span>
        <button @click="toggleMode" @mouseenter="showLabel = true" @mouseleave="showLabel = false"
            class="hover:bg-gray-100 dark:hover:bg-gray-400 px-2 py-1 text-gray-500 rounded-full">
            {{ nextModeicons[nextMode] }}
        </button>
    </div>
</template>

<script setup>
const colorMode = useColorMode()

const showLabel = ref(false)

const modes = reactive([
    'system',
    'light',
    'dark',
])

const nextModeicons = reactive({
    system: '🌓',
    light: '🌕',
    dark: '🌑',
})

const nextMode = computed(() => {
    const current = modes.findIndex(item => item === colorMode.preference)
    return current === modes.length - 1 ? modes[0] : modes[current + 1]
})

const toggleMode = () => colorMode.preference = nextMode.value
</script>