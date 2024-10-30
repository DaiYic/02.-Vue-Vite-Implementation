<template>
  <div class="home">
    <EventCard 
      v-for="event in events" 
      :key="event.id" 
      :event="event" 
    />
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import EventCard from '@/components/EventCard.vue';
import type { Event } from '@/types/types'; // 确保路径正确

// 定义一个事件数组，每个事件都是一个对象，包含所有必要的信息
const events = ref<Event[]>([
  {
    id: 1,
    category: 'Animal Welfare',
    title: 'Cat Adoption Day',
    description: 'Find your new feline friend at this event.',
    location: 'Meow Town',
    date: 'January 28, 2022',
    time: '12:00',
    petsAllowed: true,
    organizer: 'Kat Laydee'
  },
  // ...其他事件对象
]);
</script>

<style scoped>
.home {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
  padding: 20px;
}
</style>