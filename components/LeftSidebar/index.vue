<template>
    <div class="flex flex-col items-center h-screen">
        <div :class="defaultTransition"
            class="p-2 my-2 cursor-pointer hover:bg-blue-50 dark:hover:bg-white/20 rounded-full w-min gap-2">
            <nuxt-link to="/">
                <div class="w-8 h-8">
                    <img class="dark:invert min-w-full min-h-full" src="/logo/x.svg" alt="x logo" />
                </div>
            </nuxt-link>
        </div>
        <Tab text="Home" is-active>
            <HomeIcon />
        </Tab>
        <Tab text="something else"></Tab>

    </div>
</template>
<script setup lang="ts">
    import { HomeIcon } from '@heroicons/vue/20/solid'
    import Tab from './Tab.vue';
    const { defaultTransition } = useTailwindConfig()
</script>