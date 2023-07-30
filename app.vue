<template>
  <div :class="{ 'dark': darkmode }">
    <div class="bg-white dark:bg-dim-900">
      <div class="min-h-full">
        <div class="grid grid-cols-12 lg:gap-5 mx-auto max-w-7xl sm:px-6 lg:px-8">
          <!-- Left Sidebar -->
          <div class="min-h-screen  border-2 border-red-500 md:block xs:col-span-1 xl:col-span-2">
            <div class="sticky top-0">
              <LeftSidebar />
            </div>
          </div>
          <!-- Main -->
          <!-- Right Sidebar -->
        </div>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
  import LeftSidebar from './components/LeftSidebar/index.vue'
  const darkmode = ref(false)
</script>
