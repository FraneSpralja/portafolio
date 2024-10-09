<template>
    <h3>
        Take a look at my GitHub projects!
    </h3>
    <section v-if="status === 'pending'">
        Loading
    </section>
    <section v-else-if="error">
        Something went wrong... try again
    </section>
    <section v-else>
        <ul class="grid grid-cols-1 gap-4">
            <li v-for="repository in repos" :key="repository.id"
                class="project-item border border-gray-200 rounded-sm p-4 font-mono hover:bg-gray-100">
                <a :href="repository.html_url" target="_blank">
                    <div class="flex items-center justify-between">
                        <span class="font-semibold">
                            {{ repository.name }}
                        </span>
                        <small>
                            {{ repository.description }}
                        </small>
                    </div>
                </a>
            </li>
        </ul>
    </section>
</template>

<script setup>

const { error, status, data } = await useFetch('https://api.github.com/users/FraneSpralja/repos')

const repos = computed(() => data.value.filter(repo => repo.description))
</script>

<style scoped>
html.dark {
    .project-item {
        @apply hover:text-slate-950;
    }
}
</style>