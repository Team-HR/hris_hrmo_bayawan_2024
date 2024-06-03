<script setup lang="ts">
    import LoginLayout from '@/Layouts/LoginLayout.vue';
    import LoginForm from '@/Components/Forms/LoginForm.vue'
</script>

<template>
    <LoginLayout>
        <div class="flex justify-center md:justify-end py-4 px-4 md:px-24 md:py-10">

            <div>
                <LoginForm />
            </div>
        </div>
    </LoginLayout>
</template>