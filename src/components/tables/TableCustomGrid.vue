<template>
  <q-card class="no-shadow" bordered>
    <q-card-section>
      <div class="text-h6 text-grey-8">
        Custom Grid View
      </div>
    </q-card-section>
    <q-separator/>
    <q-card-section class="q-pa-none">
      <q-table grid :rows="data" :columns="columns" hide-bottom>
        <template v-slot:item="props">
          <div class="q-pa-xs col-xs-12 col-sm-6 col-md-4 col-lg-3">
            <card-profile :avatar="props.row.avatar" :name="props.row.name" :des="props.row.des"></card-profile>
          </div>
        </template>
      </q-table>
    </q-card-section>
  </q-card>
</template>

<script>
import {defineComponent} from 'vue'

import CardProfile from "components/cards/CardProfile.vue";


const columns = [
  {name: 'Name', label: 'Name', field: 'name', sortable: true, align: 'left'},
  {name: 'Crated Date', label: 'Crated Date', field: 'Crated_Date', sortable: true, align: 'left'},
  {name: 'Project', label: 'Project', field: 'Project', sortable: true, align: 'left'},
  {name: 'Action', label: '', field: 'Action', sortable: false, align: 'center'}
];

const data = [
  {
    name: 'Traore Mariam',
    Crated_Date: '15/3/2020',
    Project: 'e-commerce',
    avatar: 'AVATAR.jpg',
    progress: 80,
    des: 'Solutions Developer'
  },
  
];

export default defineComponent({
  name: "TableCustomGrid",
  components: {CardProfile},
  setup() {
    return {
      columns,
      data
    }
  }
})
</script>

<style scoped>

</style>
