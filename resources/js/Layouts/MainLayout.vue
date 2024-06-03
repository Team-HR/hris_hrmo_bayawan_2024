<script setup lang="ts">
import Navbar from '@/Components/Navbar.vue';
</script>

<template>
    <div class="max-w-3xl h-screen">
        <div class="absolute">
            <Navbar />
        </div>
        
        <div>
            <slot />
        </div>
        
    </div>
</template>