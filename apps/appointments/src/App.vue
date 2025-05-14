<template>
  <div class="min-h-screen bg-gray-100 py-10">
    <div class="max-w-xl mx-auto bg-white rounded-lg shadow p-6">
      <h1 class="text-2xl font-bold mb-4 text-blue-700">Upcoming Appointments</h1>
      <ul>
        <li
          v-for="appointment in appointments"
          :key="appointment.id"
          class="mb-4 p-4 border rounded hover:bg-blue-50"
        >
          <div class="font-semibold">{{ appointment.date }} at {{ appointment.time }}</div>
          <div class="text-gray-600">Doctor: {{ appointment.doctor }}</div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const appointments = ref([
  { id: 1, date: '2025-05-20', time: '10:00 AM', doctor: 'Dr. Smith' },
  { id: 2, date: '2025-05-22', time: '2:30 PM', doctor: 'Dr. Lee' },
  { id: 3, date: '2025-05-25', time: '9:00 AM', doctor: 'Dr. Patel' }
])
</script>