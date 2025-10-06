<script setup>
import Grid from '../Grid.vue'
import { gymHealthFacts } from '../../utils/index.js'
const randomFact = Math.floor(Math.random() * gymHealthFacts.length)
const fact = gymHealthFacts[randomFact]
</script>

<template>
      <section id="dashboard">
            <div class="card tip-container">
                  <h2>Welcom Smoldier</h2>
                  <div>
                        <p class="tip">
                              <strong>Daily Tip</strong> <br />
                              {{ fact }}
                        </p>
                  </div>
                  <button>
                        Start Workout &rarr;
                  </button>
            </div>
            <Grid />
      </section>


</template>

<style scoped>
.tip-container,
.tip-container div,
#dashboard {
      display: flex;
}

.tip-container,
#dashboard {
      flex-direction: column;
}

#dashboard {
      gap: 2rem;
}

.tip-container {
      gap: 0.5rem;
}

@media (min-width: 640px) {
      .tip-container {
            gap: 1rem;
      }
}
</style>
