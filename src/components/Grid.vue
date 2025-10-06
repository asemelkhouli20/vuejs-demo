<script setup>
import { workoutProgram } from '../utils/index.js'
const workoutTypes = ['Push', 'Pull', 'Legs']
</script>

<template>
      <section id="grid">
            <button class="card-button plan-card" 
                  v-for="(workout, workoutIndex) in Object.keys(workoutProgram)"
                  :key="workoutIndex"
                  >
                  <div>
                        <p>Day {{ workoutIndex < 9 ? `0${workoutIndex + 1}` : workoutIndex + 1 }}</p>
                        <i class="fa-solid fa-dumbbell" v-if="workoutIndex % 3 === 0"></i>
                        <i class="fa-solid fa-weight-hanging" v-if="workoutIndex % 3 === 1"></i>
                        <i class="fa-solid fa-bolt" v-if="workoutIndex % 3 === 2"></i>
                  </div>
                  <h3>{{ workoutTypes[workoutIndex % 3] }}</h3>
            </button>
      </section>

</template>

<style scoped>
#grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0,1fr));
      gap: 1rem;
}
#grid button {
      width: 100%;
}
.plan-card {
      display: flex;
      flex-direction: column;
}
.plan-card div {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap : 1rem;
}
.plan-card div p {
      text-align: left;
}
@media (min-width: 640px) {
      #grid {
            grid-template-columns: repeat(4, minmax(0,1fr));
      }
}
</style>
