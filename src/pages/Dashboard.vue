<template>
  <q-page class="q-pa-sm">

    <card-social icon_position="left"/>

    <card-charts/>

    <div class="row q-col-gutter-sm  q-py-sm">
      <tab-social/>
      <card-with-image/>
    </div>

    <div class="row q-col-gutter-sm  q-pb-sm">
      <todo-list/>

      <card-time-line/>
    </div>

    <table-visits/>
  </q-page>
</template>

<script>
import {defineComponent,defineAsyncComponent} from 'vue'

export default defineComponent({
  name: 'PageIndex',
  components: {
    CardSocial: defineAsyncComponent(() => import('components/cards/CardSocial.vue')),
    CardCharts: defineAsyncComponent(() => import('components/cards/CardCharts.vue')),
    TabSocial: defineAsyncComponent(() => import('components/tabs/TabSocial.vue')),
    CardWithImage: defineAsyncComponent(() => import('components/cards/CardWithImage.vue')),
    CardTimeLine: defineAsyncComponent(() => import('components/cards/CardTimeLine.vue')),
    TodoList: defineAsyncComponent(() => import('components/list/TodoList.vue')),
    TableVisits: defineAsyncComponent(() => import('components/tables/TableVisits.vue')),
  },
  setup() {
    return {
      mode: 'list',
      messages: [
        {
          id: 5,
          name: 'Traore Mariam',
          msg: ' -- I\'ll be in your neighborhood doing errands this\n' +
            '            weekend. Do you want to grab brunch?',
          avatar: 'AVATAR.jpg',
          time: '10:42 PM'
        }, {
          id: 6,
          name: 'Traore Mariam',
          msg: ' -- I\'ll be in your neighborhood doing errands this\n' +
            '            weekend. Do you want to grab brunch?',
          avatar: 'AVATAR.jpg',
          time: '11:17 AM'
        }, {
          id: 1,
          name: 'Traore',
          msg: ' -- I\'ll be in your neighborhood doing errands this\n' +
            '            weekend. Do you want to grab brunch?',
          avatar: 'AVATAR.jpg',
          time: '5:17 AM'
        }, {
          id: 2,
          name: 'traore',
          msg: ' -- I\'ll be in your neighborhood doing errands this\n' +
            '            weekend. Do you want to grab brunch?',
          avatar: 'AVATAR.jpg',
          time: '5:17 AM'
        }, {
          id: 3,
          name: 'Razvan Stoenescu',
          msg: ' -- I\'ll be in your neighborhood doing errands this\n' +
            '            weekend. Do you want to grab brunch?',
          avatar: 'AVATAR.jpg',
          time: '5:17 AM'
        }
      ],
    }
  },

})
</script>
