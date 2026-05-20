<script setup lang="ts">
import Calendar from './Dashboard/Calendar.vue';
import PieChart from './Dashboard/PieChart.vue';
import BarChart from './Dashboard/BarChart.vue';

</script>

<template>
    <div class="grid grid-cols-2 gap-x-2 gap-y-3 mt-3">
        <PieChart/>
        <BarChart/>
        <Calendar class="col-span-2"/>
    </div>
</template>