<template>
    <nuxt-link to="#" class="flex items-center p-3 rounded-full">
        <div class="h-6 w-6">
            <slot ></slot>
        </div>
        <div class="ml-4 text-xl" :class="isActiveClass">
            {{ $props.text }}
        </div>
    </nuxt-link>
</template>

<script setup lang="ts">
    const props = withDefaults(defineProps<{ isActive?: boolean, text: string }>(), {
        isActive: false
    })

    const isActiveClass = computed(() => props.isActive ? "font-semibold" : "font-normal")

</script>