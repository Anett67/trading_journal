<script setup lang="ts">
defineOptions({
  tags: ['donutcharts', 'basic']
})

const data = [
  { name: 'profits', percentage: 65 },
  { name: 'losses', percentage: 25 },
]

const categories = {
    profits: {
    name: 'Gains',
    color: '#61BA82'
  },
  losses: {
    name: 'Pertes',
    color: '#E94643'
  },
}

</script>

<template>
    <UCard title="Win Rate">
        <DonutChart
            :categories="categories"
            :data="data.map((i) => i.percentage)"
            :height="200"
            :hide-legend="true"
            :type="DonutType.Full"
            :radius="0"
        >
            <div class="text-center">
                <div class="font-semibold">
                    {{ data.find((item) => item.name === 'profits')?.percentage }} %
                </div>
            </div>
        </DonutChart>
    </UCard>
</template>