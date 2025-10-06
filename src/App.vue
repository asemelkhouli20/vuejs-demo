<script setup>
import Welcome from './components/pages/Welcome.vue'
import Dashboard from './components/pages/Dashboard.vue'
import Workout from './components/pages/Workout.vue'
import Layout from './components/layouts/Layout.vue'
import { ref } from 'vue'

const selectedDisplayPage = ref(3)
</script>

<template>
      <Layout>
            <!-- Page 1 -->
            <Welcome v-if="selectedDisplayPage === 1" />
            <!-- Page 2 -->
            <Dashboard v-if="selectedDisplayPage === 2" />
            <!-- Page 3 -->
            <Workout v-if="selectedDisplayPage === 3" />
      </Layout>

</template>

<style scoped></style>
