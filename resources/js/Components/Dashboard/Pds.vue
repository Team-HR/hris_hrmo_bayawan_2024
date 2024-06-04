<script setup lang="ts">
    import { ref } from 'vue';
    import PersonalInformation from '@/Components/Dashboard/Partials/PersonalInformation.vue';
    import Family from '@/Components/Dashboard/Partials/Family.vue';
    import Education from '@/Components/Dashboard/Partials/Education.vue';
    import Eligibility from '@/Components/Dashboard/Partials/Eligibility.vue';
    import WorkExperiences from '@/Components/Dashboard/Partials/WorkExperiences.vue';
    import VoluntaryWorks from '@/Components/Dashboard/Partials/VoluntaryWorks.vue';
    import Trainings from '@/Components/Dashboard/Partials/Trainings.vue';
    import OtherInformation from '@/Components/Dashboard/Partials/OtherInformation.vue';

    const activeNavItem = ref<number>(0);
    const subPartialItems = [
        {name:"Personal", key:0, content: PersonalInformation},
        {name:"Family", key:1, content: Family},
        {name:"Education", key:2, content: Education},
        {name:"Eligibility", key:3, content: Eligibility},
        {name:"Work Experiences", key:4, content: WorkExperiences},
        {name:"Voluntary Works", key:5, content: VoluntaryWorks},
        {name:"Trainings", key:6, content: Trainings},
        {name:"Other Information", key:7, content: OtherInformation},
    ]

    const setActiveNavItem = (key: number) => {
        activeNavItem.value = key;
    };
</script>

<template>
    <ul className="menu menu-vertical lg:menu-horizontal hidden lg:auto">
        <li 
            v-for="item in subPartialItems" 
            :key="item.key"
            :class="{ 'bg-base-300': activeNavItem === item.key}"
            @click="setActiveNavItem(item.key)"
        >
            <a>{{ item.name }}</a>
        </li>
    </ul>

    <select class="select select-bordered w-full block lg:hidden" @change="event => setActiveNavItem(parseInt((event.target as HTMLSelectElement).value))">
        <option 
            v-for="item in subPartialItems" 
            :key="item.key" 
            :value="item.key"
            :selected="item.key === activeNavItem"
        >{{ item.name }}</option>
    </select>

    <div>
        <component 
            v-for="item in subPartialItems"
            :is="item.content" 
            :key="item.key"
            v-show="activeNavItem === item.key"
        />
    </div>
</template>