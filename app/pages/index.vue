<script setup lang="ts">
import type { TabsItem } from '@nuxt/ui';


const items = ref<TabsItem[]>([
  {
    label: 'Tableau de bord',
    content: 'This is the account content.',
    icon: 'mdi-view-dashboard'
  },
  {
    label: 'Tableau',
    content: 'This is the password content.',
    icon: 'mdi-table-of-contents'
  },
  {
    label: 'Comptes',
    content: 'This is the password content.',
    icon: 'mdi-account-group'
  }
])

</script>

<template>
    <UContainer>
        <UTabs :content="false" :items="items" class="w-full cursor-pointer" />
    </UContainer>
</template>