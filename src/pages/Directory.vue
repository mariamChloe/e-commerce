<template>
  <q-page class="q-pa-sm">
    <div class="row q-col-gutter-sm">
      <div class="col-lg-4 col-md-4 col-xs-12 col-sm-12" v-for="(data,index) in card_data">
        <directory-card class="col-lg-4 fit col-md-4 col-sm-12 col-xs-12" :avatar="data.avatar" :name="data.name"
                        :des="data.des"
                        :email="data.email"></directory-card>
      </div>
    </div>
  </q-page>
</template>

<script>
import {defineComponent, defineAsyncComponent} from 'vue'

const card_data = [
  {
    name: 'Traore Mariam',
    Crated_Date: '15/3/2024',
    Project: 'my app',
        avatar: 'AVATAR.jpg',

    progress: 80,
    des: 'Developer full-stack',
    email: 'mariam.traorechloe@gmail.com'
  },
 
];

export default defineComponent({
  name: "Directory",
  components: {
    DirectoryCard: defineAsyncComponent(() => import('components/cards/DirectoryCard.vue'))
  },
  setup() {
    return {
      card_data
    }
  }
})
</script>

<style scoped>

</style>
