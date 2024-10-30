<template>
  <div class="event-card">
    <h2>{{ event.title }}</h2>
    <p>Category: {{ event.category }}</p>
    <p>Location: {{ event.location }}</p>
    <p>Date: {{ event.date }}</p>
    <p>Time: {{ event.time }}</p>
    <p>Pets allowed: {{ event.petsAllowed ? 'Yes' : 'No' }}</p>
    <p>Organizer: {{ event.organizer }}</p>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue';
import type { Event } from '@/types/types'; // 确保路径正确

defineProps<{
  event: Event
}>();
</script>

<style scoped>
.event-card {
  padding: 20px;
  width: 250px;
  cursor: pointer;
  border: 1px solid #39495c;
  margin-bottom: 18px;
  background-color: #fff;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.event-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 8px rgba(0,0,0,0.2);
}
</style>