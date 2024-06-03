<script setup lang="ts">
    import MainLayout from '@/Layouts/MainLayout.vue';
    import LoginForm from '@/Components/Forms/LoginForm.vue'
</script>

<template>
    <MainLayout>
        <div class="relative h-screen bg-no-repeat bg-cover bg-center" style="background-image: url('/images/layered-waves-haikei.svg');">
            <div class="flex justify-center md:justify-end py-4 px-4 md:px-24 md:py-10 h-fullbg-opacity-75">
                <div class="max-w-md w-full pt-16">
                    <LoginForm />
                </div>
            </div>
        </div>
    </MainLayout>
</template>
