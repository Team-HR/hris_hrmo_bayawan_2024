<script setup lang="ts">
    import Navbar from '@/Components/Navbar.vue';
</script>

<template>
    <div class="max-w-3xl">
        <div class="fixed z-50 w-full bg-base-100">
            <Navbar />
        </div>
        
        <div class="pb-4">
            <slot />
        </div>
    </div>
</template>