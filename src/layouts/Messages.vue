<template>
  <div>
    <q-item style="max-width: 420px" v-for="msg in messages" :key="msg.id" clickable v-ripple>
      <q-item-section avatar>
        <q-avatar>
          <img :src="msg.avatar">
        </q-avatar>
      </q-item-section>

      <q-item-section>
        <q-item-label>{{ msg.name }}</q-item-label>
        <q-item-label caption lines="1">{{ msg.msg }}</q-item-label>
      </q-item-section>

      <q-item-section side>
        {{ msg.time }}
      </q-item-section>
    </q-item>
  </div>
</template>

<script>
import {defineComponent} from 'vue'

export default defineComponent({
  name: "Messages",
  setup() {
    return {
      messages: [
        {
          id: 5,
          name: 'Mariam',
          msg: ' -- I\'ll be in your neighborhood doing errands this\n' +
            '            weekend. Do you want to grab brunch?',
          avatar: 'AVATAR.jpg',
          time: '10:42 PM'
        }, {
          id: 6,
          name: 'Mariam',
          msg: ' -- I\'ll be in your neighborhood doing errands this\n' +
            '            weekend. Do you want to grab brunch?',
          avatar: 'AVATAR.jpg',
          time: '11:17 AM'
        }, {
          id: 1,
          name: 'Mariam',
          msg: ' -- I\'ll be in your neighborhood doing errands this\n' +
            '            weekend. Do you want to grab brunch?',
          avatar: 'AVATAR.jpg',
          time: '5:17 AM'
        }, {
          id: 2,
          name: 'Mariam',
          msg: ' -- I\'ll be in your neighborhood doing errands this\n' +
            '            weekend. Do you want to grab brunch?',
          avatar: 'AVATAR.jpg',
          time: '5:17 AM'
        }, {
          id: 3,
          name: 'MARIAM',
          msg: ' -- I\'ll be in your neighborhood doing errands this\n' +
            '            weekend. Do you want to grab brunch?',
          avatar: 'AVATAR.jpg',
          time: '5:17 AM'
        }
      ],
    }
  }
})
</script>

<style scoped>

</style>
