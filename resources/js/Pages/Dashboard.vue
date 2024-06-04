<script setup lang="ts">
    import DashboardLayout from '@/Layouts/DashboardLayout.vue';
    import ProfileCard from '@/Components/ProfileCard.vue'
    import { ref } from 'vue';
    import Pds from "@/Components/Dashboard/Pds.vue"

    const activeNavItem = ref<number>(0);

    const dashboardNavItems = [
        {name: "PDS", navId: 0, content: Pds },
        {name: "Personality", navId: 1, content: Pds  },
        {name: "Competencies", navId: 2, content: Pds},
        {name: "Calendar", navId: 3, content: Pds},
        {name: "Appointment", navId: 4, content: Pds},
        {name: "Service Records", navId: 5, content: Pds},
        {name: "Leave Records", navId: 6, content: Pds},
        {name: "Hr Cores", navId: 7, content: Pds},
    ];

    const setActiveNavItem = (navId: number) => {
        activeNavItem.value = navId;
    }

</script>

<template>
    <DashboardLayout>
        <div class="pt-16 px-2 md:px-8 flex flex-col gap-4">
            
            <div class="flex flex-col gap-4">
                <ProfileCard />
            </div>         
            <div class="card bg-base-100 p-4 shadow-2xl">
                <div class="join join-vertical w-full">
                    <div class="collapse collapse-arrow join-item border border-base-300" v-for="item in dashboardNavItems" :key="item.navId"   @click="setActiveNavItem(item.navId)" >
                        <input type="radio" name="my-accordion-4" :checked="item.navId === activeNavItem" /> 
                        <div class="collapse-title text-xl font-medium">
                            {{ item.name }}
                        </div>
                        <div class="collapse-content"> 
                            <component :is="item.content" />
                        </div>
                    </div>
                </div>
            </div>

        </div>
    </DashboardLayout>
</template>
