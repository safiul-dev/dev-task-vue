<template>
    <button  v-show="this.isActive" @click="this.isActive = false" class="bg-gray-600 rounded-full w-60 h-10 ml-4 flex justify-between items-center px-2 text-white text-md font-semibold">
        <h1>Balances</h1>
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
            <path stroke-linecap="round" stroke-linejoin="round" d="M19 9l-7 7-7-7" />
        </svg>
    </button>
    <div v-show="!this.isActive" class="relative">
        <Navbare @changeMenu="() =>  this.isActive = true" />
    </div>
</template>

<script>
import Navbare from './Navbare.vue';
export default {
    components: { Navbare },
    data: function () {
        return {
            isActive: true
        }
    },
    methods: {
        changeMenu () {
            this.isActive = true;
        }
    }
}
</script>

<style>

</style>