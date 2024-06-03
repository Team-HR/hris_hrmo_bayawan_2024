<script setup lang="ts">
import Navbar from '@/Components/Navbar.vue';
</script>

<template>
    <div class="max-w-3xl">
        <Navbar />
        <slot />
    </div>
</template>