<script setup>
import EventCard from '@/components/EventCard.vue';
import { ref } from 'vue';
const events = ref([
    {
      id: 234234,
      category: 'origami convention',
      title: 'Fold That',
      description: 'Starting journey for new folders',
      location: 'Brighton',
      date: 'January 4, 2024',
      time: '12:00',
      petsAllowed: true,
      organizer: 'Satoshi Kamiya'
    },
    {
      id: 5928101,
      category: 'animal welfare',
      title: 'Cat Adoption Day',
      description: 'Find your new feline',
      location: 'London',
      date: 'January 28, 2023',
      time: '12:00',
      petsAllowed: true,
      organizer: 'John Scott'
    },
    {
      id: 4428101,
      category: 'I.T.',
      title: 'Js for All',
      description: 'code your first app using just js',
      location: 'Madrid',
      date: 'March 7, 2023',
      time: '15:00',
      petsAllowed: false,
      organizer: 'Addi Osmani'
    },
    ],)
</script>

<template>
  <div class="events">
    <EventCard v-for="event in events" :key="event.id" :event="event"></EventCard>
  </div>
</template>

<style scoped>
.events{
  display: flex;
  flex-direction: column;
  align-items: center;
}

</style>