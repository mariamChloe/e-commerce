<template>
  <q-page class="q-pa-sm">
    <div class="text-h6 q-ma-md">Pagination and Filters</div>
    <q-separator/>

    <CardPagination></CardPagination>

    <list-pagination></list-pagination>

    <basic-filter></basic-filter>

  </q-page>
</template>

<script>
import {defineComponent, defineAsyncComponent} from 'vue';

export default defineComponent({
  name: "Pagination",
  components: {
    BasicFilter: defineAsyncComponent(() => import('components/paginations/BasicFilter.vue')),
    ListPagination: defineAsyncComponent(() => import('components/paginations/ListPagination.vue')),
    CardPagination: defineAsyncComponent(() => import('components/paginations/CardPagination.vue'))
  },
})
</script>

<style scoped>

</style>
