<script setup lang="ts">
import type { TabsItem } from '@nuxt/ui';
import Dashboard from '~/components/Dashboard.vue';
import List from '~/components/List.vue';
import Accounts from '~/components/Accounts.vue';

const route = useRoute()
const router = useRouter()

const items = ref<TabsItem[]>([
  {
    label: 'Tableau de bord',
    content: 'dashboard',
    icon: 'mdi-view-dashboard'
  },
  {
    label: 'Tableau',
    icon: 'mdi-table-of-contents',
    content: 'list',
  },
  {
    label: 'Comptes',
    icon: 'mdi-account-group',
    content: 'accounts',

  }
])

const components = {
  'dashboard': Dashboard,
  'list': List,
  'accounts': Accounts
}

</script>

<template>
    <UContainer>
        <UTabs :items="items" class="w-full cursor-pointer" >
            <template #content="{ item }">
              <component v-if="item.content" :is="components[item.content]"></component>
            </template>
        </UTabs>
    </UContainer>
</template>