<script setup lang="ts">
import EventCard from '@/components/EventCard.vue'
import type { Event } from '@/types'
import { ref, onMounted } from 'vue'
import axios from 'axios'

 const events = ref<Event[]>(null)

onMounted(() => {
  axios
    .get('https://my-json-server.typicode.com/DaiYic/03db/events')
   .then((response) => {
    events.value = response.data
    })
    .catch((error) => {
      console.error('There was an error!', error)
    })
})

const events = ref<Event[]>(null)
</script>

<template>
  <h1>Events For Good</h1>
  <!-- new element -->

  <div class="events">
    <EventCard v-for="event in events" :key="event.id" :event="event" />
  </div>
</template>

<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
